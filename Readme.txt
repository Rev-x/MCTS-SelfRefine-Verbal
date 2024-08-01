run the model like this for example 

somefile.py

            from mcts_llama import mcts

            # Define your query and ground truth
            query = "If you are running a race and pass the person in second place, what place are you in now?"
            ground_truth_answer = "you are now in second place, If you are running a race and pass the person in second place, you take over their position. Initially, you are in third place because the second-place runner is directly ahead of you. When you pass the second-place runner, you move up one position, effectively taking their place. Consequently, the person you passed moves to third place, and you are now in second place. The person who was in first place remains ahead of you, so your new position is second place."


            # Define your model name
            model_name = 'ollama-model-name'  # Replace with your actual model name

            # Run MCT
            best_response = mcts(model_name=model_name, query=query, ground_truth=ground_truth_answer, iterations=2)

            print(best_response)