---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967012"
---
# <span data-ttu-id="9ac6a-101">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="9ac6a-101">Get-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="9ac6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ac6a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac6a-103">取得裝置上的磁片卷。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-103">Gets volumes on a device.</span></span>

## <span data-ttu-id="9ac6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ac6a-104">SYNTAX</span></span>

### <span data-ttu-id="9ac6a-105">IdentifyByParentObject</span><span class="sxs-lookup"><span data-stu-id="9ac6a-105">IdentifyByParentObject</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9ac6a-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="9ac6a-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ac6a-107">說明</span><span class="sxs-lookup"><span data-stu-id="9ac6a-107">DESCRIPTION</span></span>
<span data-ttu-id="9ac6a-108">**AzureStorSimpleDeviceVolume** Cmdlet 會取得指定的卷容器或具有指定名稱的卷的卷清單。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-108">The **Get-AzureStorSimpleDeviceVolume** cmdlet gets a list of volumes for a specified volume container, or volume that has the specified name.</span></span>
<span data-ttu-id="9ac6a-109">傳回的物件包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="9ac6a-109">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="9ac6a-110">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-110">**AccessType**</span></span>
- <span data-ttu-id="9ac6a-111">**AcrList**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-111">**AcrList**</span></span>
- <span data-ttu-id="9ac6a-112">**AppType**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-112">**AppType**</span></span>
- <span data-ttu-id="9ac6a-113">**DataContainer**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-113">**DataContainer**</span></span>
- <span data-ttu-id="9ac6a-114">**DataContainerId**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-114">**DataContainerId**</span></span>
- <span data-ttu-id="9ac6a-115">**Id**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-115">**InstanceId**</span></span>
- <span data-ttu-id="9ac6a-116">**IsBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-116">**IsBackupEnabled**</span></span>
- <span data-ttu-id="9ac6a-117">**IsDefaultBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-117">**IsDefaultBackupEnabled**</span></span>
- <span data-ttu-id="9ac6a-118">**IsMonitoringEnabled**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-118">**IsMonitoringEnabled**</span></span>
- <span data-ttu-id="9ac6a-119">**列名**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-119">**Name**</span></span>
- <span data-ttu-id="9ac6a-120">**Online**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-120">**Online**</span></span>
- <span data-ttu-id="9ac6a-121">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-121">**OperationInProgress**</span></span>
- <span data-ttu-id="9ac6a-122">**SizeInBytes**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-122">**SizeInBytes**</span></span>
- <span data-ttu-id="9ac6a-123">**VSN**</span><span class="sxs-lookup"><span data-stu-id="9ac6a-123">**VSN**</span></span>

## <span data-ttu-id="9ac6a-124">示例</span><span class="sxs-lookup"><span data-stu-id="9ac6a-124">EXAMPLES</span></span>

### <span data-ttu-id="9ac6a-125">範例1：取得指定容器中的磁片</span><span class="sxs-lookup"><span data-stu-id="9ac6a-125">Example 1: Get volumes in a specified container</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

<span data-ttu-id="9ac6a-126">這個命令會使用 **AzureStorSimpleDeviceVolumeContainer** Cmdlet，在名為 Contoso63-AppVm 的裝置上取得名為 Container03 的卷容器。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-126">This command gets the volume container named Container03 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="9ac6a-127">此命令會使用管線運算子，將該容器傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-127">The command uses the pipeline operator to pass that container to the current cmdlet.</span></span>
<span data-ttu-id="9ac6a-128">這個 Cmdlet 會在該容器中取得名為 Contoso63-AppVm 的裝置的所有磁片。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-128">That cmdlet gets all the volumes in that container for the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="9ac6a-129">範例2：使用名稱取得體積塊</span><span class="sxs-lookup"><span data-stu-id="9ac6a-129">Example 2: Get a volume by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

<span data-ttu-id="9ac6a-130">這個命令會在名為 Contoso63-AppVm 的裝置上取得名為 Volume18 的卷名。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-130">This command gets the volume named Volume18 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="9ac6a-131">參數</span><span class="sxs-lookup"><span data-stu-id="9ac6a-131">PARAMETERS</span></span>

### <span data-ttu-id="9ac6a-132">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9ac6a-132">-DeviceName</span></span>
<span data-ttu-id="9ac6a-133">指定要取得磁片卷的 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-133">Specifies the name of the StorSimple device from which to get volumes.</span></span>

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

### <span data-ttu-id="9ac6a-134">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9ac6a-134">-Profile</span></span>
<span data-ttu-id="9ac6a-135">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-135">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9ac6a-136">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="9ac6a-136">-VolumeContainer</span></span>
<span data-ttu-id="9ac6a-137">指定作為 **DataContainer** 物件的卷容器，包括要取得的磁片。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-137">Specifies the volume container, as a **DataContainer** object, that includes the volumes to get.</span></span>
<span data-ttu-id="9ac6a-138">若要取得 **DataContainer** ，請使用 **AzureStorSimpleDeviceVolumeContainer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-138">To obtain a **DataContainer** , use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac6a-139">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="9ac6a-139">-VolumeName</span></span>
<span data-ttu-id="9ac6a-140">指定要取得的卷名。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-140">Specifies the name of the volume to get.</span></span>

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

### <span data-ttu-id="9ac6a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac6a-141">CommonParameters</span></span>
<span data-ttu-id="9ac6a-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac6a-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac6a-144">輸入</span><span class="sxs-lookup"><span data-stu-id="9ac6a-144">INPUTS</span></span>

### <span data-ttu-id="9ac6a-145">DataContainer</span><span class="sxs-lookup"><span data-stu-id="9ac6a-145">DataContainer</span></span>
<span data-ttu-id="9ac6a-146">這個 Cmdlet 接受包含要取得的音量的 **DataContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-146">This cmdlet accepts a **DataContainer** object that contains the volume to get.</span></span>

## <span data-ttu-id="9ac6a-147">輸出</span><span class="sxs-lookup"><span data-stu-id="9ac6a-147">OUTPUTS</span></span>

### <span data-ttu-id="9ac6a-148">VirtualDisk、IList\<VirtualDisk\></span><span class="sxs-lookup"><span data-stu-id="9ac6a-148">VirtualDisk, IList\<VirtualDisk\></span></span>
<span data-ttu-id="9ac6a-149">如果您指定 *VolumeName* 參數，這個 Cmdlet 會傳回 **VirtualDisk** 物件。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-149">This cmdlet returns a **VirtualDisk** object if you specify the *VolumeName* parameter.</span></span>
<span data-ttu-id="9ac6a-150">如果您指定 *VolumeContainer* ，這個 Cmdlet 會傳回 **IList \<VirtualDisk\>** 物件。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-150">If you specify the *VolumeContainer* , this cmdlet returns an **IList\<VirtualDisk\>** object.</span></span>

## <span data-ttu-id="9ac6a-151">筆記</span><span class="sxs-lookup"><span data-stu-id="9ac6a-151">NOTES</span></span>

## <span data-ttu-id="9ac6a-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ac6a-152">RELATED LINKS</span></span>

[<span data-ttu-id="9ac6a-153">新-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="9ac6a-153">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="9ac6a-154">移除-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="9ac6a-154">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="9ac6a-155">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="9ac6a-155">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="9ac6a-156">AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="9ac6a-156">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


