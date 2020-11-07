---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967895"
---
# <span data-ttu-id="83ee0-101">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="83ee0-101">Remove-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="83ee0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="83ee0-103">刪除現有的儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="83ee0-103">Deletes an existing storage account credential.</span></span>

## <span data-ttu-id="83ee0-104">句法</span><span class="sxs-lookup"><span data-stu-id="83ee0-104">SYNTAX</span></span>

### <span data-ttu-id="83ee0-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="83ee0-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="83ee0-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="83ee0-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="83ee0-107">說明</span><span class="sxs-lookup"><span data-stu-id="83ee0-107">DESCRIPTION</span></span>
<span data-ttu-id="83ee0-108">AzureStorSimpleStorageAccountCredential Cmdlet 會刪除現有 **的** 儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="83ee0-108">The **Remove-AzureStorSimpleStorageAccountCredential** cmdlet deletes an existing storage account credential.</span></span>
<span data-ttu-id="83ee0-109">依名稱指定帳戶，或使用 **AzureStorSimpleStorageAccountCredential** Cmdlet 來取得要刪除的 **StorageAccountCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="83ee0-109">Specify an account by name or use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet to obtain a **StorageAccountCredential** object to delete.</span></span>

## <span data-ttu-id="83ee0-110">示例</span><span class="sxs-lookup"><span data-stu-id="83ee0-110">EXAMPLES</span></span>

### <span data-ttu-id="83ee0-111">範例1：移除儲存空間帳號憑證</span><span class="sxs-lookup"><span data-stu-id="83ee0-111">Example 1: Remove a storage account credential</span></span>
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

<span data-ttu-id="83ee0-112">這個命令會移除名為 ContosoStorage07 的儲存空間帳戶的帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="83ee0-112">This command removes the account credential for the storage account named ContosoStorage07.</span></span>
<span data-ttu-id="83ee0-113">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="83ee0-113">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="83ee0-114">Cmdlet 會移除認證，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="83ee0-114">The cmdlet removes the credential without prompting your for confirmation.</span></span>

### <span data-ttu-id="83ee0-115">範例2：使用管線運算子移除儲存空間帳號憑證</span><span class="sxs-lookup"><span data-stu-id="83ee0-115">Example 2: Remove a storage account credential by using the pipeline operator</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

<span data-ttu-id="83ee0-116">這個命令會使用 **AzureStorSimpleStorageAccountCredential** Cmdlet 取得名為 ContosoStorage07 的儲存空間帳戶，然後將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83ee0-116">This command gets the storage account named ContosoStorage07 by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet, and then passes that object to the current cmdlet.</span></span>
<span data-ttu-id="83ee0-117">目前的 Cmdlet 會移除該儲存空間帳戶的認證。</span><span class="sxs-lookup"><span data-stu-id="83ee0-117">The current cmdlet removes the credential for that storage account.</span></span>
<span data-ttu-id="83ee0-118">這個命令會指定 *WaitForComplete* 參數。</span><span class="sxs-lookup"><span data-stu-id="83ee0-118">This command specifies the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="83ee0-119">除非完成移除作業，否則 Cmdlet 不會將控制權傳回給主控台。</span><span class="sxs-lookup"><span data-stu-id="83ee0-119">The cmdlet does not return control to the console until it completes the remove operation.</span></span>

## <span data-ttu-id="83ee0-120">參數</span><span class="sxs-lookup"><span data-stu-id="83ee0-120">PARAMETERS</span></span>

### <span data-ttu-id="83ee0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="83ee0-121">-Force</span></span>
<span data-ttu-id="83ee0-122">表示此 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="83ee0-122">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ee0-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="83ee0-123">-Profile</span></span>
<span data-ttu-id="83ee0-124">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="83ee0-124">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ee0-125">SAC</span><span class="sxs-lookup"><span data-stu-id="83ee0-125">-SAC</span></span>
<span data-ttu-id="83ee0-126">指定認證（作為 **StorageAccountCredential** 物件）來移除。</span><span class="sxs-lookup"><span data-stu-id="83ee0-126">Specifies credential, as a **StorageAccountCredential** object, to remove.</span></span>
<span data-ttu-id="83ee0-127">若要取得 **StorageAccountCredential** 物件，請使用 **AzureStorSimpleStorageAccountCredential** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83ee0-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83ee0-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="83ee0-128">-StorageAccountName</span></span>
<span data-ttu-id="83ee0-129">指定要刪除的儲存空間帳號憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="83ee0-129">Specifies the name of the storage account credential to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ee0-130">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="83ee0-130">-WaitForComplete</span></span>
<span data-ttu-id="83ee0-131">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="83ee0-131">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ee0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ee0-132">CommonParameters</span></span>
<span data-ttu-id="83ee0-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83ee0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ee0-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83ee0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ee0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="83ee0-135">INPUTS</span></span>

### <span data-ttu-id="83ee0-136">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="83ee0-136">StorageAccountCredential</span></span>
<span data-ttu-id="83ee0-137">這個 Cmdlet 會使用管線接受 **StorageAccountCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="83ee0-137">This cmdlet accepts a **StorageAccountCredential** object by using the pipeline.</span></span>

## <span data-ttu-id="83ee0-138">輸出</span><span class="sxs-lookup"><span data-stu-id="83ee0-138">OUTPUTS</span></span>

### <span data-ttu-id="83ee0-139">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="83ee0-139">TaskStatusInfo</span></span>
<span data-ttu-id="83ee0-140">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="83ee0-140">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="83ee0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="83ee0-141">NOTES</span></span>

## <span data-ttu-id="83ee0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="83ee0-142">RELATED LINKS</span></span>

[<span data-ttu-id="83ee0-143">AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="83ee0-143">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="83ee0-144">新-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="83ee0-144">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="83ee0-145">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="83ee0-145">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="83ee0-146">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="83ee0-146">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


