---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967222"
---
# <span data-ttu-id="f9c4e-101">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f9c4e-101">Start-AzureStorSimpleDeviceFailoverJob</span></span>

## <span data-ttu-id="f9c4e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9c4e-102">SYNOPSIS</span></span>
<span data-ttu-id="f9c4e-103">啟動大量容器群組的容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-103">Initiates a failover operation of volume container groups.</span></span>

## <span data-ttu-id="f9c4e-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9c4e-104">SYNTAX</span></span>

### <span data-ttu-id="f9c4e-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="f9c4e-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f9c4e-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="f9c4e-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f9c4e-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="f9c4e-107">IdentifyByName</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f9c4e-108">說明</span><span class="sxs-lookup"><span data-stu-id="f9c4e-108">DESCRIPTION</span></span>
<span data-ttu-id="f9c4e-109">**AzureStorSimpleDeviceFailoverJob** Cmdlet 會將一個或多個卷容器群組的容錯移轉作業從一個裝置移到另一個裝置。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-109">The **Start-AzureStorSimpleDeviceFailoverJob** cmdlet initiates a failover operation of one or more volume container groups from one device to another.</span></span>

## <span data-ttu-id="f9c4e-110">示例</span><span class="sxs-lookup"><span data-stu-id="f9c4e-110">EXAMPLES</span></span>

### <span data-ttu-id="f9c4e-111">範例1：針對命名的裝置和命名目標裝置啟動容錯移轉作業</span><span class="sxs-lookup"><span data-stu-id="f9c4e-111">Example 1: Start a failover job for a named device and named target device</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="f9c4e-112">這個命令會透過 **AzureStorSimpleFailoverVolumeContainers** Cmdlet，透過名為 ChewD_App7 的裝置取得容錯移轉磁片容器。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-112">This command gets the failover volume containers for the device named ChewD_App7 by using the **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet.</span></span>
<span data-ttu-id="f9c4e-113">該命令會將結果傳遞到 **物件** 的 Cmdlet，該指令會放下 **IsDCGroupEligibleForDR** 屬性不是 $True 值的那些容器。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-113">The command passes the results to the **Where-Object** cmdlet, which drops those containers that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="f9c4e-114">如需詳細資訊，請輸入 `Get-Help Where-Object` 。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-114">For more information, type `Get-Help Where-Object`.</span></span>
<span data-ttu-id="f9c4e-115">目前的 Cmdlet 會針對其餘的容錯移轉磁片容器啟動容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-115">The current cmdlet starts failover jobs for the remaining failover volume containers.</span></span>
<span data-ttu-id="f9c4e-116">命令會指定裝置名稱和目標裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-116">The command specifies the device name and target device name.</span></span>
<span data-ttu-id="f9c4e-117">此命令會傳回 Cmdlet 啟動作業的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-117">The command returns the instance ID of the job that the cmdlet starts.</span></span>

### <span data-ttu-id="f9c4e-118">範例2：針對由識別碼指定的裝置和目標裝置啟動容錯移轉作業</span><span class="sxs-lookup"><span data-stu-id="f9c4e-118">Example 2: Start a failover job for a device and target device specified by ID</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="f9c4e-119">這個命令會使用 **AzureStorSimpleFailoverVolumeContainers** ，透過名為 ChewD_App7 的裝置，取得容錯移轉磁片容器。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-119">This command gets the failover volume containers for the device named ChewD_App7 by using **Get-AzureStorSimpleFailoverVolumeContainers**.</span></span>
<span data-ttu-id="f9c4e-120">該命令會將結果傳遞到物件，該 **物件** 會放下 containters 的值不是 **IsDCGroupEligibleForDR** 屬性的 $True。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-120">The command passes the results to **Where-Object** , which drops those containters that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="f9c4e-121">Cmdlet 會將結果傳遞到 **Select 物件** Cmdlet，以選取要傳遞到目前 Cmdlet 的第一個物件。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-121">The cmdlet passes the results to the **Select-Object** cmdlet, which selects the first object to pass to the current cmdlet.</span></span>
<span data-ttu-id="f9c4e-122">如需詳細資訊，請輸入 `Get-Help Select-Object` 。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-122">For more information, type `Get-Help Select-Object`.</span></span>
<span data-ttu-id="f9c4e-123">目前的 Cmdlet 會針對選取的 [容錯移轉磁片] 容器啟動容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-123">The current cmdlet starts failover jobs for the selected failover volume container.</span></span>
<span data-ttu-id="f9c4e-124">命令會指定裝置識別碼和目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-124">The command specifies the device ID and target device ID.</span></span>
<span data-ttu-id="f9c4e-125">此命令會傳回 Cmdlet 啟動作業的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-125">The command returns the instance ID of the job that the cmdlet starts.</span></span>

## <span data-ttu-id="f9c4e-126">參數</span><span class="sxs-lookup"><span data-stu-id="f9c4e-126">PARAMETERS</span></span>

### <span data-ttu-id="f9c4e-127">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f9c4e-127">-DeviceId</span></span>
<span data-ttu-id="f9c4e-128">指定要有卷容器群組的 StorSimple 裝置的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-128">Specifies the instance ID of the StorSimple device on which the volume container groups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c4e-129">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f9c4e-129">-DeviceName</span></span>
<span data-ttu-id="f9c4e-130">指定要有卷容器群組的 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-130">Specifies the name of the StorSimple device on which the volume container groups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c4e-131">-Force</span><span class="sxs-lookup"><span data-stu-id="f9c4e-131">-Force</span></span>
<span data-ttu-id="f9c4e-132">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f9c4e-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f9c4e-133">-Profile</span></span>
<span data-ttu-id="f9c4e-134">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="f9c4e-135">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="f9c4e-135">-TargetDeviceId</span></span>
<span data-ttu-id="f9c4e-136">指定此 Cmdlet 針對磁片容器群組進行容錯移轉之 StorSimple 裝置的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-136">Specifies the instance ID of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c4e-137">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="f9c4e-137">-TargetDeviceName</span></span>
<span data-ttu-id="f9c4e-138">指定此 Cmdlet 針對磁片容器群組進行容錯移轉之 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-138">Specifies the name of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c4e-139">-VolumecontainerGroups</span><span class="sxs-lookup"><span data-stu-id="f9c4e-139">-VolumecontainerGroups</span></span>
<span data-ttu-id="f9c4e-140">指定此 Cmdlet 容錯移轉至另一個裝置的卷容器群組清單。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-140">Specifies the list of volume container groups that this cmdlet fails over to another device.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9c4e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9c4e-141">CommonParameters</span></span>
<span data-ttu-id="f9c4e-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9c4e-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9c4e-144">輸入</span><span class="sxs-lookup"><span data-stu-id="f9c4e-144">INPUTS</span></span>

### <span data-ttu-id="f9c4e-145">清單\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="f9c4e-145">List\<DataContainerGroup\></span></span>
<span data-ttu-id="f9c4e-146">您可以將大量容器群組的清單輸送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9c4e-146">You can pipe a list of volume container groups to this cmdlet.</span></span>

## <span data-ttu-id="f9c4e-147">輸出</span><span class="sxs-lookup"><span data-stu-id="f9c4e-147">OUTPUTS</span></span>

### <span data-ttu-id="f9c4e-148">字串</span><span class="sxs-lookup"><span data-stu-id="f9c4e-148">String</span></span>

## <span data-ttu-id="f9c4e-149">筆記</span><span class="sxs-lookup"><span data-stu-id="f9c4e-149">NOTES</span></span>

## <span data-ttu-id="f9c4e-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9c4e-150">RELATED LINKS</span></span>

[<span data-ttu-id="f9c4e-151">AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="f9c4e-151">Get-AzureStorSimpleFailoverVolumeContainers</span></span>](./Get-AzureStorSimpleFailoverVolumeContainers.md)


