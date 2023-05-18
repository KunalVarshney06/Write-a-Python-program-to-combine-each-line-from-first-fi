# Write-a-Python-program-to-combine-each-line-from-first-fi
def combine_files(file1_path, file2_path, output_file_path):
    try:
        with open(file1_path, 'r') as file1, open(file2_path, 'r') as file2, open(output_file_path, 'w') as output_file:
            for line1, line2 in zip(file1, file2):
                combined_line = line1.strip() + ' ' + line2.strip() + '\n'
                output_file.write(combined_line)
        print("Files combined successfully.")
    except FileNotFoundError:
        print("File not found.")
    except IOError:
        print("An error occurred while combining the files.")

# Example usage
file1_path = 'path/to/your/file1.txt'  # Replace with the actual path of the first file
file2_path = 'path/to/your/file2.txt'  # Replace with the actual path of the second file
output_file_path = 'path/to/your/output.txt'  # Replace with the actual path of the output file
combine_files(file1_path, file2_path, output_file_path)
