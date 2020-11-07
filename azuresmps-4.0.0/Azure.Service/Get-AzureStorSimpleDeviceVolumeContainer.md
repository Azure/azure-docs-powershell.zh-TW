---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967009"
---
# <span data-ttu-id="2adaa-101">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="2adaa-101">Get-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="2adaa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2adaa-102">SYNOPSIS</span></span>
<span data-ttu-id="2adaa-103">取得裝置上的音量容器。</span><span class="sxs-lookup"><span data-stu-id="2adaa-103">Gets volume containers on a device.</span></span>

## <span data-ttu-id="2adaa-104">句法</span><span class="sxs-lookup"><span data-stu-id="2adaa-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2adaa-105">說明</span><span class="sxs-lookup"><span data-stu-id="2adaa-105">DESCRIPTION</span></span>
<span data-ttu-id="2adaa-106">**AzureStorSimpleDeviceVolumeContainer** Cmdlet 會取得裝置上的卷容器清單，或具有指定名稱的卷容器。</span><span class="sxs-lookup"><span data-stu-id="2adaa-106">The **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet gets a list of volume containers on a device, or volume container that has the specified name.</span></span>
<span data-ttu-id="2adaa-107">傳回的物件包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="2adaa-107">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="2adaa-108">**BandwidthRate**</span><span class="sxs-lookup"><span data-stu-id="2adaa-108">**BandwidthRate**</span></span>
- <span data-ttu-id="2adaa-109">**Encryption.encryptionkey**</span><span class="sxs-lookup"><span data-stu-id="2adaa-109">**EncryptionKey**</span></span>
- <span data-ttu-id="2adaa-110">**Id**</span><span class="sxs-lookup"><span data-stu-id="2adaa-110">**InstanceId**</span></span>
- <span data-ttu-id="2adaa-111">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="2adaa-111">**IsDefault**</span></span>
- <span data-ttu-id="2adaa-112">**IsEncryptionEnabled**</span><span class="sxs-lookup"><span data-stu-id="2adaa-112">**IsEncryptionEnabled**</span></span>
- <span data-ttu-id="2adaa-113">**列名**</span><span class="sxs-lookup"><span data-stu-id="2adaa-113">**Name**</span></span>
- <span data-ttu-id="2adaa-114">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="2adaa-114">**OperationInProgress**</span></span>
- <span data-ttu-id="2adaa-115">**屬於**</span><span class="sxs-lookup"><span data-stu-id="2adaa-115">**Owned**</span></span>
- <span data-ttu-id="2adaa-116">**PrimaryStorageAccountCredential**</span><span class="sxs-lookup"><span data-stu-id="2adaa-116">**PrimaryStorageAccountCredential**</span></span>
- <span data-ttu-id="2adaa-117">**SecretsEncryptionThumbprint**</span><span class="sxs-lookup"><span data-stu-id="2adaa-117">**SecretsEncryptionThumbprint**</span></span>
- <span data-ttu-id="2adaa-118">**VolumeCount**</span><span class="sxs-lookup"><span data-stu-id="2adaa-118">**VolumeCount**</span></span>

## <span data-ttu-id="2adaa-119">示例</span><span class="sxs-lookup"><span data-stu-id="2adaa-119">EXAMPLES</span></span>

### <span data-ttu-id="2adaa-120">範例1：取得裝置上的所有容器</span><span class="sxs-lookup"><span data-stu-id="2adaa-120">Example 1: Get all the containers on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

<span data-ttu-id="2adaa-121">這個命令會在名為 8600-Bravo 001 的裝置上取得卷容器清單。</span><span class="sxs-lookup"><span data-stu-id="2adaa-121">This command gets a list of the volume containers on the device named 8600-Bravo 001.</span></span>

### <span data-ttu-id="2adaa-122">範例2：使用其名稱取得容器</span><span class="sxs-lookup"><span data-stu-id="2adaa-122">Example 2: Get a container by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

<span data-ttu-id="2adaa-123">這個命令會在名為 Contoso63-AppVm 的裝置上，取得名為 Container08 的卷容器。</span><span class="sxs-lookup"><span data-stu-id="2adaa-123">This command gets the volume container named Container08 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="2adaa-124">參數</span><span class="sxs-lookup"><span data-stu-id="2adaa-124">PARAMETERS</span></span>

### <span data-ttu-id="2adaa-125">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2adaa-125">-DeviceName</span></span>
<span data-ttu-id="2adaa-126">指定 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2adaa-126">Specifies the name of a StorSimple device.</span></span>
<span data-ttu-id="2adaa-127">這個 Cmdlet 會從裝置中取得此參數指定的音量容器。</span><span class="sxs-lookup"><span data-stu-id="2adaa-127">This cmdlet gets volume containers from the device that this parameter specifies.</span></span>

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

### <span data-ttu-id="2adaa-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="2adaa-128">-Profile</span></span>
<span data-ttu-id="2adaa-129">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2adaa-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="2adaa-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="2adaa-130">-VolumeContainerName</span></span>
<span data-ttu-id="2adaa-131">指定要取得的卷容器名稱。</span><span class="sxs-lookup"><span data-stu-id="2adaa-131">Specifies the name of the volume container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2adaa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2adaa-132">CommonParameters</span></span>
<span data-ttu-id="2adaa-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2adaa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2adaa-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2adaa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2adaa-135">輸入</span><span class="sxs-lookup"><span data-stu-id="2adaa-135">INPUTS</span></span>

### <span data-ttu-id="2adaa-136">所有</span><span class="sxs-lookup"><span data-stu-id="2adaa-136">None</span></span>

## <span data-ttu-id="2adaa-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2adaa-137">OUTPUTS</span></span>

### <span data-ttu-id="2adaa-138">DataContainer、IList\<DataContainer\></span><span class="sxs-lookup"><span data-stu-id="2adaa-138">DataContainer, IList\<DataContainer\></span></span>
<span data-ttu-id="2adaa-139">如果您指定 *VolumeContainerName* 參數，這個 Cmdlet 會傳回 **DataContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="2adaa-139">This cmdlet returns a **DataContainer** object, if you specify the *VolumeContainerName* parameter.</span></span>
<span data-ttu-id="2adaa-140">如果您沒有指定該參數，這個 Cmdlet 會傳回 **IList \<DataContainer\>** 物件。</span><span class="sxs-lookup"><span data-stu-id="2adaa-140">If you do not specify that parameter, this cmdlet returns an **IList\<DataContainer\>** object.</span></span>

## <span data-ttu-id="2adaa-141">筆記</span><span class="sxs-lookup"><span data-stu-id="2adaa-141">NOTES</span></span>

## <span data-ttu-id="2adaa-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="2adaa-142">RELATED LINKS</span></span>

[<span data-ttu-id="2adaa-143">新-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="2adaa-143">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="2adaa-144">移除-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="2adaa-144">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


