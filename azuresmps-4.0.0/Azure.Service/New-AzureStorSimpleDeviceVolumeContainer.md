---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5605F11E-EEA0-4C32-8445-2E001D56BC47
online version: ''
schema: 2.0.0
ms.openlocfilehash: e364692858cf190b48b61f4d38fbf483d229ffb7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966966"
---
# <span data-ttu-id="3766d-101">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="3766d-101">New-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="3766d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3766d-102">SYNOPSIS</span></span>
<span data-ttu-id="3766d-103">建立一個卷容器。</span><span class="sxs-lookup"><span data-stu-id="3766d-103">Creates a volume container.</span></span>

## <span data-ttu-id="3766d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3766d-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainerName <String>
 -PrimaryStorageAccountCredential <StorageAccountCredentialResponse> -BandWidthRateInMbps <Int32>
 [-EncryptionEnabled <Boolean>] [-EncryptionKey <String>] [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3766d-105">說明</span><span class="sxs-lookup"><span data-stu-id="3766d-105">DESCRIPTION</span></span>
<span data-ttu-id="3766d-106">**新的-AzureStorSimpleDeviceVolumeContainer** Cmdlet 會建立一個卷容器。</span><span class="sxs-lookup"><span data-stu-id="3766d-106">The **New-AzureStorSimpleDeviceVolumeContainer** cmdlet creates a volume container.</span></span>
<span data-ttu-id="3766d-107">您必須將儲存帳號憑證與新的卷容器建立關聯。</span><span class="sxs-lookup"><span data-stu-id="3766d-107">You must associate a storage account credential with the new volume container.</span></span>
<span data-ttu-id="3766d-108">若要取得儲存空間帳號憑證，請使用 **AzureStorSimpleStorageAccountCredential** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3766d-108">To obtain a storage account credential, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

## <span data-ttu-id="3766d-109">示例</span><span class="sxs-lookup"><span data-stu-id="3766d-109">EXAMPLES</span></span>

### <span data-ttu-id="3766d-110">範例1：建立容器</span><span class="sxs-lookup"><span data-stu-id="3766d-110">Example 1: Create a container</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount" | New-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" -BandWidthRateInMbps 256
VERBOSE: ClientRequestId: 96a4ccd4-f2a9-4820-8bc8-e6b7b56dce0d_PS
VERBOSE: ClientRequestId: 90be20db-098a-4f2b-a6da-9da6f533a846_PS
VERBOSE: ClientRequestId: 410fd33a-8fa3-4ae5-a1bf-1b6da9b34ffc_PS
VERBOSE: Storage Access Credential with name ContosoAccount found! 
VERBOSE: ClientRequestId: 0a6d1008-ba1f-43b2-a424-9c86be2fb83b_PS
VERBOSE: ClientRequestId: 08f0d657-a130-4a25-8090-270c58b479dc_PS
VERBOSE: ClientRequestId: 0f3e894a-b031-467c-a258-41b74c89cf18_PS
5b192120-9df0-40ed-b75e-b4e728bd37ef
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
5b192120-9df0-40ed-b75e-b4e728bd37ef for tracking the task's status
```

<span data-ttu-id="3766d-111">這個命令會使用 **AzureStorSimpleStorageAccountCredential** Cmdlet 來取得名為 ContosoAccount 帳戶的儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="3766d-111">This command gets the storage account credential for the account named ContosoAccount by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>
<span data-ttu-id="3766d-112">命令會使用管線運算子，將認證傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3766d-112">The command passes the credential to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3766d-113">這個 Cmdlet 使用該 Cmdlet 的認證，在名為 Contoso63-AppVm 的裝置上建立名為 Container08 的容器。</span><span class="sxs-lookup"><span data-stu-id="3766d-113">This cmdlet uses the credential from that cmdlet to create the container named Container08 on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="3766d-114">這個命令會啟動作業，然後傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="3766d-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="3766d-115">若要查看作業的狀態，請使用 **AzureStorSimpleTask** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3766d-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="3766d-116">參數</span><span class="sxs-lookup"><span data-stu-id="3766d-116">PARAMETERS</span></span>

### <span data-ttu-id="3766d-117">-BandWidthRateInMbps</span><span class="sxs-lookup"><span data-stu-id="3766d-117">-BandWidthRateInMbps</span></span>
<span data-ttu-id="3766d-118">指定以百萬位元/秒為單位 (Mbps) 的頻寬速率。</span><span class="sxs-lookup"><span data-stu-id="3766d-118">Specifies the bandwidth rate in megabits per second (Mbps).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CloudBandwidthInMbps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3766d-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3766d-119">-DeviceName</span></span>
<span data-ttu-id="3766d-120">指定要在其上建立卷容器的 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3766d-120">Specifies the name of the StorSimple device on which to create the volume container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3766d-121">-EncryptionEnabled</span><span class="sxs-lookup"><span data-stu-id="3766d-121">-EncryptionEnabled</span></span>
<span data-ttu-id="3766d-122">指出是否要啟用加密。</span><span class="sxs-lookup"><span data-stu-id="3766d-122">Indicates whether to enable encryption.</span></span>

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

### <span data-ttu-id="3766d-123">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="3766d-123">-EncryptionKey</span></span>
<span data-ttu-id="3766d-124">指定加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="3766d-124">Specifies the encryption key.</span></span>

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

### <span data-ttu-id="3766d-125">-PrimaryStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3766d-125">-PrimaryStorageAccountCredential</span></span>
<span data-ttu-id="3766d-126">指定認證（作為 **StorageAccountCredential** 物件）以與新的卷容器建立關聯。</span><span class="sxs-lookup"><span data-stu-id="3766d-126">Specifies the credential, as a **StorageAccountCredential** object, to associate with the new volume container.</span></span>
<span data-ttu-id="3766d-127">若要取得 **StorageAccountCredential** 物件，請使用 **AzureStorSimpleStorageAccountCredential** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3766d-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: (All)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3766d-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3766d-128">-Profile</span></span>
<span data-ttu-id="3766d-129">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3766d-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="3766d-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="3766d-130">-VolumeContainerName</span></span>
<span data-ttu-id="3766d-131">指定要建立之卷容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3766d-131">Specifies the name of the volume container to create.</span></span>

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

### <span data-ttu-id="3766d-132">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="3766d-132">-WaitForComplete</span></span>
<span data-ttu-id="3766d-133">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="3766d-133">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="3766d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3766d-134">CommonParameters</span></span>
<span data-ttu-id="3766d-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3766d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3766d-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3766d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3766d-137">輸入</span><span class="sxs-lookup"><span data-stu-id="3766d-137">INPUTS</span></span>

### <span data-ttu-id="3766d-138">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3766d-138">StorageAccountCredential</span></span>
<span data-ttu-id="3766d-139">這個 Cmdlet 接受 **PrimaryStorageAccountCredential** 物件，以與卷容器建立關聯。</span><span class="sxs-lookup"><span data-stu-id="3766d-139">This cmdlet accepts a **PrimaryStorageAccountCredential** object to associate with the volume container.</span></span>

## <span data-ttu-id="3766d-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3766d-140">OUTPUTS</span></span>

### <span data-ttu-id="3766d-141">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="3766d-141">TaskStatusInfo</span></span>
<span data-ttu-id="3766d-142">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="3766d-142">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="3766d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="3766d-143">NOTES</span></span>

## <span data-ttu-id="3766d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="3766d-144">RELATED LINKS</span></span>

[<span data-ttu-id="3766d-145">AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="3766d-145">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="3766d-146">移除-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="3766d-146">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="3766d-147">AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3766d-147">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="3766d-148">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="3766d-148">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


