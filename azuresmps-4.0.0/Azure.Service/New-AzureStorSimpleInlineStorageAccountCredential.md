---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BC68C60C-86E3-4857-95AE-1A915A841F7D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 803bc4006e5be8582183248c22115fcd51862d13
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966963"
---
# <span data-ttu-id="7add0-101">New-AzureStorSimpleInlineStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7add0-101">New-AzureStorSimpleInlineStorageAccountCredential</span></span>

## <span data-ttu-id="7add0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7add0-102">SYNOPSIS</span></span>
<span data-ttu-id="7add0-103">建立內嵌儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="7add0-103">Creates an inline storage account credential.</span></span>

## <span data-ttu-id="7add0-104">句法</span><span class="sxs-lookup"><span data-stu-id="7add0-104">SYNTAX</span></span>

```
New-AzureStorSimpleInlineStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 [-Endpoint <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7add0-105">說明</span><span class="sxs-lookup"><span data-stu-id="7add0-105">DESCRIPTION</span></span>
<span data-ttu-id="7add0-106">**AzureStorSimpleInlineStorageAccountCredential** Cmdlet 會建立內嵌的 Azure 儲存空間帳號憑證物件。</span><span class="sxs-lookup"><span data-stu-id="7add0-106">The **New-AzureStorSimpleInlineStorageAccountCredential** cmdlet creates an inline Azure storage account credential object.</span></span>
<span data-ttu-id="7add0-107">這個 Cmdlet 會建立一個虛擬身分認證物件。</span><span class="sxs-lookup"><span data-stu-id="7add0-107">This cmdlet creates a dummy credential object.</span></span>
<span data-ttu-id="7add0-108">您可以使用 Windows PowerShell 管線，在同一個命令中使用 **新的 AzureStorSimpleDeviceVolumeContainer** Cmdlet 和目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7add0-108">You can use the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet and the current cmdlet in the same command by using the Windows PowerShell pipeline.</span></span>
<span data-ttu-id="7add0-109">實際的儲存帳號憑證物件是在建立大量容器時建立的。</span><span class="sxs-lookup"><span data-stu-id="7add0-109">The actual storage account credential object is created as part of creation of the volume container.</span></span>

## <span data-ttu-id="7add0-110">示例</span><span class="sxs-lookup"><span data-stu-id="7add0-110">EXAMPLES</span></span>

### <span data-ttu-id="7add0-111">範例1：建立內嵌的儲存空間帳號憑證</span><span class="sxs-lookup"><span data-stu-id="7add0-111">Example 1: Create a storage account credential inline</span></span>
```
PS C:\>New-AzureStorSimpleInlineStorageAccountCredential -Name "contoso76" -Key x6o/tpZh8Coo8Tteo0NHLksTOKr/P9Vufo0LZNGdPGVTSUu00/p6ta1w9gRbVBNjzN8aa504kH2zkEsfUme+kw== | New-AzureStorSimpleDeviceVolumeContainer -Name "VolumeContainer_06" -DeviceName Contoso_App3 -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "Key22" -WaitForComplete
VERBOSE: ClientRequestId: 535d24d5-1ed8-4759-92b2-dd492f94e23e_PS
VERBOSE: ClientRequestId: f32fc069-96c9-4fd9-a71a-0e62d81f25d8_PS
VERBOSE: ClientRequestId: 4376a931-89f5-448f-92bd-b2f7234244c9_PS
VERBOSE: ClientRequestId: 980109d4-7d76-40d0-ae3c-db539e2cb486_PS
VERBOSE: Encryption in progress... 
VERBOSE: Creating StorageAccountCredential inline
VERBOSE: Found storage account with name : contoso76
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: d4f8a5de-bf81-4773-b6e6-edb034284cf4_PS


JobId        : 2dec64d3-b30d-4d35-adb3-12689b235b79
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: abd4082a-2eda-42ad-8cb3-5864dd2f7d1f_PS
BandwidthRate                   : 256
EncryptionKey                   : SK23I39L7GvoLce7u63TMT/A/V/TW8JXe+PoXKEKzwsr3t/h7tdqV1EpfaK0DGO/qo5b2PLCagFHAxnZEiejg
                                  jtF9TcyK+aLyzEnkqtM+eNRJmgANzJ9C/5L6Ubp+eSWiy+U/pyZygxPrb37e0yFg+qbHV9R9Qi+afBpHD9Gsi
                                  rhURuOc/idWG29eaEifuRzn/zEjvwJ2pEyYLcsuL+ftfRYZom69XO+cRDv5yT3xdNI/dAod/5YUaf1IhJl8wR
                                  cWjqyr00NxlCI03hTgH2sFyTFZWc07S2KI5K5n3rmCL6vGT76SRgNFeUxGz3v06/VoBhdmv9vDfrEz5UkW04d
                                  Qw==
InstanceId                      : a72bf4bb-0f0a-4ec2-a8b1-c4548825f522
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VolumneContainer_06
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="7add0-112">這個命令會以內嵌方式建立儲存帳號憑證，然後使用管線運算子將它傳送到 **AzureStorSimpleDeviceVolumeContainer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7add0-112">This command creates a storage account credential inline, and then passes it to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7add0-113">該容器使用虛擬認證來建立大量容器。</span><span class="sxs-lookup"><span data-stu-id="7add0-113">That container uses the dummy credential to create a volume container.</span></span>

## <span data-ttu-id="7add0-114">參數</span><span class="sxs-lookup"><span data-stu-id="7add0-114">PARAMETERS</span></span>

### <span data-ttu-id="7add0-115">-端點</span><span class="sxs-lookup"><span data-stu-id="7add0-115">-Endpoint</span></span>
<span data-ttu-id="7add0-116">指定儲存空間帳戶的 Azure 儲存端點。</span><span class="sxs-lookup"><span data-stu-id="7add0-116">Specifies the Azure storage endpoint for the storage account.</span></span>

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

### <span data-ttu-id="7add0-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7add0-117">-Profile</span></span>
<span data-ttu-id="7add0-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7add0-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7add0-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7add0-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7add0-120">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7add0-120">-StorageAccountKey</span></span>
<span data-ttu-id="7add0-121">以純文字格式指定儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="7add0-121">Specifies the account key of the storage account in plain text.</span></span>
<span data-ttu-id="7add0-122">金鑰會以加密格式進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="7add0-122">The key is transferred in encrypted format.</span></span>

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

### <span data-ttu-id="7add0-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7add0-123">-StorageAccountName</span></span>
<span data-ttu-id="7add0-124">指定現有儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7add0-124">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="7add0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7add0-125">CommonParameters</span></span>
<span data-ttu-id="7add0-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7add0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7add0-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7add0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7add0-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7add0-128">INPUTS</span></span>

### <span data-ttu-id="7add0-129">所有</span><span class="sxs-lookup"><span data-stu-id="7add0-129">None</span></span>

## <span data-ttu-id="7add0-130">輸出</span><span class="sxs-lookup"><span data-stu-id="7add0-130">OUTPUTS</span></span>

### <span data-ttu-id="7add0-131">StorageAccountCredentialResponse</span><span class="sxs-lookup"><span data-stu-id="7add0-131">StorageAccountCredentialResponse</span></span>
<span data-ttu-id="7add0-132">這個 Cmdlet 會傳回 **CloudType** 物件，其中包含下欄欄位：</span><span class="sxs-lookup"><span data-stu-id="7add0-132">This cmdlet returns a **CloudType** object, which contains the following fields:</span></span> 

- <span data-ttu-id="7add0-133">**主機名稱** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-133">**Hostname**.</span></span>
<span data-ttu-id="7add0-134">**字串** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-134">**String**.</span></span> 
- <span data-ttu-id="7add0-135">**InstanceId** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-135">**InstanceId**.</span></span>
<span data-ttu-id="7add0-136">**字串** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-136">**String**.</span></span> 
- <span data-ttu-id="7add0-137">**IsDefault** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-137">**IsDefault**.</span></span>
<span data-ttu-id="7add0-138">**布林值** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-138">**Boolean**.</span></span> 
- <span data-ttu-id="7add0-139">**位置** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-139">**Location**.</span></span>
<span data-ttu-id="7add0-140">**字串** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-140">**String**.</span></span> 
- <span data-ttu-id="7add0-141">**[登** 入]。</span><span class="sxs-lookup"><span data-stu-id="7add0-141">**Login**.</span></span>
<span data-ttu-id="7add0-142">**字串** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-142">**String**.</span></span> 
- <span data-ttu-id="7add0-143">[ **名稱** ]。</span><span class="sxs-lookup"><span data-stu-id="7add0-143">**Name**.</span></span>
<span data-ttu-id="7add0-144">**字串** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-144">**String**.</span></span> 
- <span data-ttu-id="7add0-145">**OperationInProgress** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-145">**OperationInProgress**.</span></span>
<span data-ttu-id="7add0-146">**OperationInProgress** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-146">**OperationInProgress**.</span></span> 
- <span data-ttu-id="7add0-147">**密碼** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-147">**Password**.</span></span>
<span data-ttu-id="7add0-148">**字串** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-148">**String**.</span></span> 
- <span data-ttu-id="7add0-149">**PasswordEncryptionCertThumbprint** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-149">**PasswordEncryptionCertThumbprint**.</span></span>
<span data-ttu-id="7add0-150">**字串** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-150">**String**.</span></span> 
- <span data-ttu-id="7add0-151">**UseSSL** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-151">**UseSSL**.</span></span>
<span data-ttu-id="7add0-152">**布林值** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-152">**Boolean**.</span></span> 
- <span data-ttu-id="7add0-153">**VolumeCount** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-153">**VolumeCount**.</span></span>
<span data-ttu-id="7add0-154">**整數** 。</span><span class="sxs-lookup"><span data-stu-id="7add0-154">**Integer**.</span></span>

## <span data-ttu-id="7add0-155">筆記</span><span class="sxs-lookup"><span data-stu-id="7add0-155">NOTES</span></span>

## <span data-ttu-id="7add0-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="7add0-156">RELATED LINKS</span></span>

[<span data-ttu-id="7add0-157">新-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7add0-157">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="7add0-158">新-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="7add0-158">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


