---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 74088389-A003-4746-8A57-2146BBA7535C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0b86da15e81fd6eca005e04fc36b5887691af4bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967297"
---
# <span data-ttu-id="23228-101">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="23228-101">Set-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="23228-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23228-102">SYNOPSIS</span></span>
<span data-ttu-id="23228-103">更新 Azure 儲存空間存取認證。</span><span class="sxs-lookup"><span data-stu-id="23228-103">Updates an Azure storage access credential.</span></span>

## <span data-ttu-id="23228-104">句法</span><span class="sxs-lookup"><span data-stu-id="23228-104">SYNTAX</span></span>

```
Set-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-StorageAccountKey <String>]
 [-UseSSL <Boolean>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="23228-105">說明</span><span class="sxs-lookup"><span data-stu-id="23228-105">DESCRIPTION</span></span>
<span data-ttu-id="23228-106">**AzureStorSimpleStorageAccountCredential** Cmdlet 會更新 StorSimple OneSDK Cmdlet 要使用的現有 Azure 儲存空間存取認證。</span><span class="sxs-lookup"><span data-stu-id="23228-106">The **Set-AzureStorSimpleStorageAccountCredential** cmdlet update an existing Azure storage access credential for use by StorSimple OneSDK cmdlets.</span></span>
<span data-ttu-id="23228-107">如需有關 StorSimple Cmdlet 如何搭配儲存帳戶使用的詳細資訊，請參閱 New-AzureStorSimpleStorageAccountCredential Cmdlet 的說明主題。</span><span class="sxs-lookup"><span data-stu-id="23228-107">For more information about how StorSimple cmdlets work with storage accounts, see the help topic for the New-AzureStorSimpleStorageAccountCredential cmdlet.</span></span>

## <span data-ttu-id="23228-108">示例</span><span class="sxs-lookup"><span data-stu-id="23228-108">EXAMPLES</span></span>

### <span data-ttu-id="23228-109">範例1：修改認證</span><span class="sxs-lookup"><span data-stu-id="23228-109">Example 1: Modify a credential</span></span>
```
PS C:\>Set-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage01" -UseSSL $False -StorageAccountKey "h9ldH4LlHJB3GujcNwgdxJACy1DaQ1Hak1bfoUBzrDqZ5DPK8+0XGbsgD+jrKfQy5PBepKpYobMViLaOC2XMdg==" -Force -WaitForComplete
VERBOSE: ClientRequestId: 20cd2b17-9cff-4ab4-a034-96d60d946295_PS
VERBOSE: ClientRequestId: a75ed193-1da5-491f-96f5-572b5461d466_PS
VERBOSE: ClientRequestId: db612c9e-e89a-404f-8406-e66e7f697cd5_PS
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: About to run a task to update your Storage Access credential! 
VERBOSE: ClientRequestId: a0995bb7-8223-4fcf-83c9-0a4f81e6a85c_PS


JobId        : 74a6172e-d47a-4824-a7fa-3eb207a76e0b
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: de04c77b-4846-45e0-9257-df501af9d4e9_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoStorage01
Name                             : ContosoStorage01
OperationInProgress              : None
Password                         : UUejow8u6ZynMm18g59883FBVtlIX6PWh6x+v15cnnkHKEAb5queTGnGOiGa/KkOqths7F/umDz+wUUB8zzq
                                   4YCi0Dm0rqPGDC4unhxvbncf+WeCEvV7qsf3pmUFdk8o96Cgl8oXgmmvYL9K6Z6ajHUdZFFlq9WqUpz2vBbz
                                   3ROxq8SRORt2DQVQP6LWojTiow1kNI/v2cs3eNvzoSgGftqzjSmhaTYu+q0o8X07eE4KwkWhQrRX24seH2Lg
                                   N9aYCQUrSxVKOAFJjdLOIBUlM48pnE7xyyZNwqngnPLt8z+mlS6JCKfo5SBKUfwmkhgDFfbVwB3jqC/sV/G6
                                   omwQ/A==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

<span data-ttu-id="23228-110">這個命令會將名為 ContosoStorage01 的儲存空間帳號憑證變更為 [不再需要 SSL]。</span><span class="sxs-lookup"><span data-stu-id="23228-110">This command changes the storage account credential named ContosoStorage01 to no longer require SSL.</span></span>

## <span data-ttu-id="23228-111">參數</span><span class="sxs-lookup"><span data-stu-id="23228-111">PARAMETERS</span></span>

### <span data-ttu-id="23228-112">-設定檔</span><span class="sxs-lookup"><span data-stu-id="23228-112">-Profile</span></span>
<span data-ttu-id="23228-113">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="23228-113">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="23228-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="23228-114">-StorageAccountKey</span></span>
<span data-ttu-id="23228-115">以純文字格式指定儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="23228-115">Specifies the access key of the storage account in plain text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23228-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="23228-116">-StorageAccountName</span></span>
<span data-ttu-id="23228-117">指定現有儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="23228-117">Specifies the name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23228-118">-UseSSL</span><span class="sxs-lookup"><span data-stu-id="23228-118">-UseSSL</span></span>
<span data-ttu-id="23228-119">指示在使用新的儲存空間帳號憑證時，是否要針對連線使用 SSL。</span><span class="sxs-lookup"><span data-stu-id="23228-119">Indicates whether to use SSL for the connection when using the new storage account credential.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23228-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="23228-120">-WaitForComplete</span></span>
<span data-ttu-id="23228-121">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="23228-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="23228-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23228-122">CommonParameters</span></span>
<span data-ttu-id="23228-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23228-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23228-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23228-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23228-125">輸入</span><span class="sxs-lookup"><span data-stu-id="23228-125">INPUTS</span></span>

### <span data-ttu-id="23228-126">所有</span><span class="sxs-lookup"><span data-stu-id="23228-126">None</span></span>

## <span data-ttu-id="23228-127">輸出</span><span class="sxs-lookup"><span data-stu-id="23228-127">OUTPUTS</span></span>

### <span data-ttu-id="23228-128">StorageAccountCredentialResponse, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="23228-128">StorageAccountCredentialResponse, TaskResponse</span></span>
<span data-ttu-id="23228-129">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **StorageAccountCredentialResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="23228-129">This cmdlet returns a **StorageAccountCredentialResponse** object, if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="23228-130">如果您沒有指定該參數，則 Cmdlet 會傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="23228-130">If you do not specify that parameter, the cmdlet returns a **TaskResponse** object.</span></span>
<span data-ttu-id="23228-131">**StorageAccountCredentialResponse** 包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="23228-131">A **StorageAccountCredentialResponse** contains the following properties:</span></span> 

- <span data-ttu-id="23228-132">**CloudType** ( **CloudType** ) </span><span class="sxs-lookup"><span data-stu-id="23228-132">**CloudType** ( **CloudType** )</span></span>
- <span data-ttu-id="23228-133">**主機名稱** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="23228-133">**Hostname** ( **String** )</span></span>
- <span data-ttu-id="23228-134">**InstanceId** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="23228-134">**InstanceId** ( **String** )</span></span>
- <span data-ttu-id="23228-135">**IsDefault** ( **布林值** ) </span><span class="sxs-lookup"><span data-stu-id="23228-135">**IsDefault** ( **Boolean** )</span></span>
- <span data-ttu-id="23228-136">**位置** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="23228-136">**Location** ( **String** )</span></span>
- <span data-ttu-id="23228-137">**登** 入 ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="23228-137">**Login** ( **String** )</span></span>
- <span data-ttu-id="23228-138">**名稱** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="23228-138">**Name** ( **String** )</span></span>
- <span data-ttu-id="23228-139">**OperationInProgress** ( **OperationInProgress** ) </span><span class="sxs-lookup"><span data-stu-id="23228-139">**OperationInProgress** ( **OperationInProgress** )</span></span>
- <span data-ttu-id="23228-140">**密碼** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="23228-140">**Password** ( **String** )</span></span>
- <span data-ttu-id="23228-141">**PasswordEncryptionCertThumbprint** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="23228-141">**PasswordEncryptionCertThumbprint** ( **String** )</span></span>
- <span data-ttu-id="23228-142">**UseSSL** ( **布林值** ) </span><span class="sxs-lookup"><span data-stu-id="23228-142">**UseSSL** ( **Boolean** )</span></span>
- <span data-ttu-id="23228-143">**VolumeCount** ( **int** ) </span><span class="sxs-lookup"><span data-stu-id="23228-143">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="23228-144">筆記</span><span class="sxs-lookup"><span data-stu-id="23228-144">NOTES</span></span>

## <span data-ttu-id="23228-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="23228-145">RELATED LINKS</span></span>

[<span data-ttu-id="23228-146">AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="23228-146">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="23228-147">新-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="23228-147">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="23228-148">移除-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="23228-148">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)


