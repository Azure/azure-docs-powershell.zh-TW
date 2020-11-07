---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BDCD6FD8-F4D5-4897-BF91-C78773DD3546
online version: ''
schema: 2.0.0
ms.openlocfilehash: f414f480328d508f0178d2536d144dceda3baab6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966959"
---
# <span data-ttu-id="8937c-101">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8937c-101">New-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="8937c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8937c-102">SYNOPSIS</span></span>
<span data-ttu-id="8937c-103">新增 Azure 儲存空間存取認證。</span><span class="sxs-lookup"><span data-stu-id="8937c-103">Adds an Azure storage access credential.</span></span>

## <span data-ttu-id="8937c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8937c-104">SYNTAX</span></span>

```
New-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 -UseSSL <Boolean> [-Endpoint <String>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8937c-105">說明</span><span class="sxs-lookup"><span data-stu-id="8937c-105">DESCRIPTION</span></span>
<span data-ttu-id="8937c-106">**新的-AzureStorSimpleStorageAccountCredential** Cmdlet 會將 Azure 儲存空間存取認證新增至 storsimple manager，以供 storsimple OneSDK Cmdlet 使用。</span><span class="sxs-lookup"><span data-stu-id="8937c-106">The **New-AzureStorSimpleStorageAccountCredential** cmdlet adds an Azure storage access credential to StorSimple manager for use by StorSimple OneSDK cmdlets.</span></span>
<span data-ttu-id="8937c-107">大部分的 StorSimple OneSDK Cmdlet 都會處理最終系結至特定儲存空間帳戶的實體，例如卷、卷容器、備份及備份原則。</span><span class="sxs-lookup"><span data-stu-id="8937c-107">Most of the StorSimple OneSDK cmdlets deal with entities that are eventually tied to a specific storage account, such as volumes, volume containers, backups, and backup policies.</span></span>
<span data-ttu-id="8937c-108">對於某些 Cmdlet，您必須提供所使用的儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="8937c-108">For some cmdlets, you must provide the credentials of the storage account in use.</span></span>
<span data-ttu-id="8937c-109">儲存帳號憑證是在 OneSDK 中建立的 access 物件，指向現有的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="8937c-109">A storage account credential is an access object created in OneSDK that points to an existing Azure storage account.</span></span>
<span data-ttu-id="8937c-110">您提供現有儲存空間帳戶的名稱和存取金鑰來建立儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="8937c-110">You provide the name and access key of an existing storage account to create a storage account credential.</span></span>
<span data-ttu-id="8937c-111">然後，您就可以將該認證物件與其他 Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="8937c-111">You can then use that credential object with other cmdlets.</span></span>

<span data-ttu-id="8937c-112">這個 Cmdlet 使用您在使用 **AzureStorSimpleResource** Cmdlet 選取資源時所提供的註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="8937c-112">This cmdlet uses the registration key that you provide when you select the resource by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>
<span data-ttu-id="8937c-113">請確定該值正確，以避免加密失敗。</span><span class="sxs-lookup"><span data-stu-id="8937c-113">Be sure that value is correct to avoid encryption failure.</span></span>
<span data-ttu-id="8937c-114">若要將註冊金鑰修改為正確的值，請使用 **Select-AzureStorSimpleResource** 。</span><span class="sxs-lookup"><span data-stu-id="8937c-114">To modify the registration key to a correct value, use **Select-AzureStorSimpleResource**.</span></span>

## <span data-ttu-id="8937c-115">示例</span><span class="sxs-lookup"><span data-stu-id="8937c-115">EXAMPLES</span></span>

### <span data-ttu-id="8937c-116">範例1：建立認證</span><span class="sxs-lookup"><span data-stu-id="8937c-116">Example 1: Create a credential</span></span>
```
PS C:\>New-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount07" -StorageAccountKey "L/eVcHtvqKjPWm5SaAJXtDlc0d69yVs0ICoZ2XIV1x0r9TqUyQyLUNS8lHvTvRmzdvQhJelav3fYyX7wyAu/SA==" -UseSSL $False -WaitForComplete
VERBOSE: ClientRequestId: f363cda4-54aa-4ee8-a3fa-00651ac86ffb_PS
VERBOSE: Found storage account with name : ContosoAccount07
VERBOSE: Storage credential verification succeeded. 
VERBOSE: ClientRequestId: 716ce6df-62b3-4d48-8e0e-b0c94eec6934_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: 19aa4ef7-2789-4817-980c-19e33d257650_PS

JobId        : 84f74c25-b742-452c-973c-43c7446e9f49
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 72bcdf37-bf06-4dac-adc9-31bb8d06475a_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : b9986714-cef4-4c3f-a719-7acfc9559320
IsDefault                        : False
Location                         : West Europe
Login                            : ContosoAccount07
Name                             : ContosoAccount07
OperationInProgress              : None

Password                         : G1sBQ6/qAN1gyRGRZVarpi7o6ToJl61sGugfeJ75yx7cwyaGLQHjrSEEwhxThbDJkxso2emAOarTe920Uufy
                                   0AmJ9NpBI5hNyIFfwS4Ff+z2WmfKOzApyeofW5Zy7GPufehe/2ondq0XG4pGt3qxHFXNVUuiaPSU6TVWEKSh
                                   hWDaksSXYMGij3DJdZDW1MA49e6Q7OY+rFujbYvi9P2OjVj8T+FbiMtMB5NnQEqE+t3k74RqPIDKU+d3h9x4
                                   rYbAksGPfMvSa0fUipwYJ+Y5/NABA6j/MfB2pNDJbvqDoa1JCX6SKiwL81wmTh78/KnDY5ST3Said5DzKEbR
                                   iYMQZg==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

<span data-ttu-id="8937c-117">這個命令會為指定的儲存空間帳戶建立儲存空間存取認證。</span><span class="sxs-lookup"><span data-stu-id="8937c-117">This command creates a storage access credential for the specified storage account.</span></span>
<span data-ttu-id="8937c-118">這個命令會指定 *WaitForComplete* 參數，因此 Cmdlet 會等到任務完成，才能將控制權傳回給主機。</span><span class="sxs-lookup"><span data-stu-id="8937c-118">This command specifies the *WaitForComplete* parameter, and, so, the cmdlet waits until the task finishes to return control to the console.</span></span>

### <span data-ttu-id="8937c-119">範例2：建立認證並查詢該任務的狀態</span><span class="sxs-lookup"><span data-stu-id="8937c-119">Example 2: Create a credential and query that status of the task</span></span>
```
PS C:\>New-AzureStorSimpleStorageAccountCredential -Name "ContosoAccount08" -Key "6BlMpSVrCQVQy3iOpkxiyY8uk/e3PiHIhadxV4qpPlKInr/eRFrGcWKDrfNC1IHj6oh0If/h3rALdZ0zuaf9cQ==" -UseSSL $True
PS C:\> Get-AzureStorSimpleTask -InstanceId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: 6104a834-ea57-4687-8e0b-1d97dc1c038b_PS
VERBOSE: Found storage account with name : ContosoAccount08
VERBOSE: Storage credential verification succeeded. 
VERBOSE: ClientRequestId: 1f686fa4-5afc-43c3-87b6-f2da7bf9e65f_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: 8acb3770-bd72-43e6-9622-481002ad40b0_PS
53816d8d-a8b5-4c1d-a177-e59007608d6d
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
53816d8d-a8b5-4c1d-a177-e59007608d6d for tracking the task's status
```

<span data-ttu-id="8937c-120">第一個命令會為指定的儲存空間帳戶建立儲存空間存取認證。</span><span class="sxs-lookup"><span data-stu-id="8937c-120">The first command creates a storage access credential for the specified storage account.</span></span>
<span data-ttu-id="8937c-121">命令會傳回任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="8937c-121">The command returns a task ID.</span></span>

<span data-ttu-id="8937c-122">第二個命令會使用 **AzureStorSimpleTask** Cmdlet 來查詢任務的狀態。</span><span class="sxs-lookup"><span data-stu-id="8937c-122">The second command queries the status of the task by using the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="8937c-123">命令會從第一個命令指定任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="8937c-123">The command specifies the task ID from the first command.</span></span>

### <span data-ttu-id="8937c-124">範例3：建立認證以與另一個 Cmdlet 搭配使用</span><span class="sxs-lookup"><span data-stu-id="8937c-124">Example 3: Create a credential to use with another cmdlet</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -Name "ContosoAccount09" | New-AzureStorSimpleDeviceVolumeContainer -Name "VC03" -DeviceName "Contoso63-AppVm" -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "<your encryption key>" -WaitForComplete
VERBOSE: ClientRequestId: b1d1e637-cd72-4a1e-95a8-4db1d0b921a7_PS
VERBOSE: ClientRequestId: 71f56ca0-1f0b-4655-9331-4849e096345a_PS
VERBOSE: ClientRequestId: fbdd5a96-c95f-4547-9bcd-376d05543348_PS
VERBOSE: Storage Access Credential with name ContosoAccount09 found! 
VERBOSE: ClientRequestId: b44e0363-9979-4e97-aeb1-d9eb4073a337_PS
VERBOSE: ClientRequestId: a6047943-b01e-44e4-a91d-5103aa80ce57_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: ac2dfd8b-922f-4e4d-8c8d-df1e2f87806c_PS


JobId        : 1cf2db5d-624f-46c4-97b9-c36451ba144e
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 9558414b-0883-4cf6-8a02-40efc7edd80d_PS
BandwidthRate                   : 256
EncryptionKey                   : g53NTgCF3SBVZzzk+9yUz5nZopvZpNr3th92ol7WRO7ZUKhodPm7WNjjHEKB0/V+JY6P68tdaF4JxF5jH58e/
                                  mCtTvnPNpOxykYFdY9GKGd9gnf+36sUPqiLFP+ONO5nN/N/zFmOeyuySsaa3gJsZG8eIiFc821yfe9m5QPbF
                                  bx/Qyu8qLl1R1LrKU7k+46IXfwQYSyclztydyuzvFUUic9kaJuR3944VLvrjvxJIbnLrYy7hsn+Gfq7ds9NFq
                                  AUILBH0+bk2uWgUlofAcE8fJ/rzDAHr8nFGWxOTJSrqAo0J3st8BN39+BcrY+zOWsMc/vKfc+Ss5PsGVGDT1r
                                  eQ==
InstanceId                      : 60c34706-ef0c-4c6f-ad90-7249f42648f7
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VC03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="8937c-125">這個命令會建立儲存帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="8937c-125">This command creates a storage account credential.</span></span>
<span data-ttu-id="8937c-126">然後，命令會使用管線運算子，將該認證傳送到 **AzureStorSimpleDeviceVolumeContainer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8937c-126">The command then passes that credential to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8937c-127">該 Cmdlet 會使用認證來建立新的卷容器。</span><span class="sxs-lookup"><span data-stu-id="8937c-127">That cmdlet creates a new volume container by using the credential.</span></span>

## <span data-ttu-id="8937c-128">參數</span><span class="sxs-lookup"><span data-stu-id="8937c-128">PARAMETERS</span></span>

### <span data-ttu-id="8937c-129">-端點</span><span class="sxs-lookup"><span data-stu-id="8937c-129">-Endpoint</span></span>
<span data-ttu-id="8937c-130">指定儲存空間帳戶的 Azure 儲存端點。</span><span class="sxs-lookup"><span data-stu-id="8937c-130">Specifies the Azure storage endpoint for the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8937c-131">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8937c-131">-Profile</span></span>
<span data-ttu-id="8937c-132">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8937c-132">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="8937c-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8937c-133">-StorageAccountKey</span></span>
<span data-ttu-id="8937c-134">以純文字格式指定儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="8937c-134">Specifies the access key of the storage account in plain text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8937c-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8937c-135">-StorageAccountName</span></span>
<span data-ttu-id="8937c-136">指定現有儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8937c-136">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="8937c-137">-UseSSL</span><span class="sxs-lookup"><span data-stu-id="8937c-137">-UseSSL</span></span>
<span data-ttu-id="8937c-138">指示在使用新的儲存空間帳號憑證時，是否要針對連線使用 SSL。</span><span class="sxs-lookup"><span data-stu-id="8937c-138">Indicates whether to use SSL for the connection when using the new storage account credential.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8937c-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="8937c-139">-WaitForComplete</span></span>
<span data-ttu-id="8937c-140">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="8937c-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="8937c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8937c-141">CommonParameters</span></span>
<span data-ttu-id="8937c-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8937c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8937c-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8937c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8937c-144">輸入</span><span class="sxs-lookup"><span data-stu-id="8937c-144">INPUTS</span></span>

### <span data-ttu-id="8937c-145">所有</span><span class="sxs-lookup"><span data-stu-id="8937c-145">None</span></span>

## <span data-ttu-id="8937c-146">輸出</span><span class="sxs-lookup"><span data-stu-id="8937c-146">OUTPUTS</span></span>

### <span data-ttu-id="8937c-147">IEnumerable \<StorageAccountCredentialResponse\> 、TaskResponse</span><span class="sxs-lookup"><span data-stu-id="8937c-147">IEnumerable\<StorageAccountCredentialResponse\>, TaskResponse</span></span>
<span data-ttu-id="8937c-148">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **StorageAccountCredentialResponse** 物件的清單。</span><span class="sxs-lookup"><span data-stu-id="8937c-148">This cmdlet returns a list of **StorageAccountCredentialResponse** objects, if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="8937c-149">如果您沒有指定該參數，則 Cmdlet 會傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="8937c-149">If you do not specify that parameter, the cmdlet returns a **TaskResponse** object.</span></span>
<span data-ttu-id="8937c-150">**StorageAccountCredentialResponse** 包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="8937c-150">A **StorageAccountCredentialResponse** contains the following properties:</span></span> 

- <span data-ttu-id="8937c-151">**CloudType** ( **CloudType** ) </span><span class="sxs-lookup"><span data-stu-id="8937c-151">**CloudType** ( **CloudType** )</span></span>
- <span data-ttu-id="8937c-152">**主機名稱** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="8937c-152">**Hostname** ( **String** )</span></span>
- <span data-ttu-id="8937c-153">**InstanceId** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="8937c-153">**InstanceId** ( **String** )</span></span>
- <span data-ttu-id="8937c-154">**IsDefault** ( **布林值** ) </span><span class="sxs-lookup"><span data-stu-id="8937c-154">**IsDefault** ( **Boolean** )</span></span>
- <span data-ttu-id="8937c-155">**位置** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="8937c-155">**Location** ( **String** )</span></span>
- <span data-ttu-id="8937c-156">**登** 入 ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="8937c-156">**Login** ( **String** )</span></span>
- <span data-ttu-id="8937c-157">**名稱** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="8937c-157">**Name** ( **String** )</span></span>
- <span data-ttu-id="8937c-158">**OperationInProgress** ( **OperationInProgress** ) </span><span class="sxs-lookup"><span data-stu-id="8937c-158">**OperationInProgress** ( **OperationInProgress** )</span></span>
- <span data-ttu-id="8937c-159">**密碼** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="8937c-159">**Password** ( **String** )</span></span>
- <span data-ttu-id="8937c-160">**PasswordEncryptionCertThumbprint** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="8937c-160">**PasswordEncryptionCertThumbprint** ( **String** )</span></span>
- <span data-ttu-id="8937c-161">**UseSSL** ( **布林值** ) </span><span class="sxs-lookup"><span data-stu-id="8937c-161">**UseSSL** ( **Boolean** )</span></span>
- <span data-ttu-id="8937c-162">**VolumeCount** ( **int** ) </span><span class="sxs-lookup"><span data-stu-id="8937c-162">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="8937c-163">筆記</span><span class="sxs-lookup"><span data-stu-id="8937c-163">NOTES</span></span>

## <span data-ttu-id="8937c-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="8937c-164">RELATED LINKS</span></span>

[<span data-ttu-id="8937c-165">AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8937c-165">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="8937c-166">移除-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8937c-166">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="8937c-167">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8937c-167">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="8937c-168">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="8937c-168">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="8937c-169">新-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8937c-169">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


