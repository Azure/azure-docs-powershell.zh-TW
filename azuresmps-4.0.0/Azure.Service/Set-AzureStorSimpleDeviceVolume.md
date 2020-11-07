---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 39E9BB88-6AD8-4B05-9498-35393E22BA30
online version: ''
schema: 2.0.0
ms.openlocfilehash: 234b1f7fa2719cc1b34e6bcd0b8e8fd340acc4af
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967864"
---
# <span data-ttu-id="65247-101">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="65247-101">Set-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="65247-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65247-102">SYNOPSIS</span></span>
<span data-ttu-id="65247-103">更新現有卷的屬性。</span><span class="sxs-lookup"><span data-stu-id="65247-103">Updates the properties of an existing volume.</span></span>

## <span data-ttu-id="65247-104">句法</span><span class="sxs-lookup"><span data-stu-id="65247-104">SYNTAX</span></span>

### <span data-ttu-id="65247-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="65247-105">IdentifyByName</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="65247-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="65247-106">IdentifyByObject</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="65247-107">說明</span><span class="sxs-lookup"><span data-stu-id="65247-107">DESCRIPTION</span></span>
<span data-ttu-id="65247-108">**AzureStorSimpleDeviceVolume** Cmdlet 會更新現有卷的屬性。</span><span class="sxs-lookup"><span data-stu-id="65247-108">The **Set-AzureStorSimpleDeviceVolume** cmdlet updates the properties of an existing volume.</span></span>
<span data-ttu-id="65247-109">這個 Cmdlet 會將一個卷集與一個或多個存取控制記錄相關聯。</span><span class="sxs-lookup"><span data-stu-id="65247-109">This cmdlet associates a volume with one or more access control records.</span></span>
<span data-ttu-id="65247-110">若要取得 **AccessControlRecord** 物件，請使用 **AzureStorSimpleAccessControlRecord** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65247-110">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="65247-111">更新卷的大小或類型。</span><span class="sxs-lookup"><span data-stu-id="65247-111">Update the size or type for the volume.</span></span>
<span data-ttu-id="65247-112">此外，更新是否要在線上建立大量磁片。</span><span class="sxs-lookup"><span data-stu-id="65247-112">Also, update whether to create the volume online.</span></span>

## <span data-ttu-id="65247-113">示例</span><span class="sxs-lookup"><span data-stu-id="65247-113">EXAMPLES</span></span>

### <span data-ttu-id="65247-114">範例1：更新卷的線上值</span><span class="sxs-lookup"><span data-stu-id="65247-114">Example 1: Update online value for a volume</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $False
VERBOSE: ClientRequestId: f2869570-ea47-4be7-801e-9c0f22f2600d_PS
VERBOSE: ClientRequestId: c70bb86a-51d3-4390-be17-4d0847641dc3_PS
VERBOSE: ClientRequestId: d20cb5b2-6b3c-4e06-af99-cada28c5e50a_PS
VERBOSE: ClientRequestId: ab6d533e-b55b-4cfb-9c58-9153295e0547_PS
de7000f1-29c7-4102-a375-b52432f9e67e
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
de7000f1-29c7-4102-a375-b52432f9e67e for tracking the task's status
```

<span data-ttu-id="65247-115">這個命令會將名為 Volume18 的卷更新為 $False 的線上值。</span><span class="sxs-lookup"><span data-stu-id="65247-115">This command updates the volume named Volume18 to have an online value of $False.</span></span>
<span data-ttu-id="65247-116">這個命令會啟動任務，然後傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="65247-116">This command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="65247-117">若要查看任務的狀態，請使用 **AzureStorSimpleTask** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65247-117">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="65247-118">範例2：修改線上值與類型</span><span class="sxs-lookup"><span data-stu-id="65247-118">Example 2: Modify online value and type</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $True -VolumeAppType ArchiveVolume 
VERBOSE: ClientRequestId: af42b02a-645e-4801-a2d7-4197511c68cf_PS
VERBOSE: ClientRequestId: 7cb4f3b4-548e-42dc-a38c-0df0911c5206_PS
VERBOSE: ClientRequestId: 7cc706ad-a58f-4939-8e78-cabae8379a51_PS
VERBOSE: ClientRequestId: 6bed21d5-12fc-4a12-a89c-120bdb5636b1_PS
aa977225-af78-4c93-b754-72704afc928f
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
aa977225-af78-4c93-b754-72704afc928f for tracking the task's status
```

<span data-ttu-id="65247-119">這個命令會更新名為 Volume18 的卷。</span><span class="sxs-lookup"><span data-stu-id="65247-119">This command updates the volume named Volume18.</span></span>
<span data-ttu-id="65247-120">它會修改類型，並將 *Online* 參數的值變更為 [$True]。</span><span class="sxs-lookup"><span data-stu-id="65247-120">It modifies the type and changes the value of the *Online* parameter to $True.</span></span>

## <span data-ttu-id="65247-121">參數</span><span class="sxs-lookup"><span data-stu-id="65247-121">PARAMETERS</span></span>

### <span data-ttu-id="65247-122">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="65247-122">-AccessControlRecords</span></span>
<span data-ttu-id="65247-123">指定要與該卷建立關聯的存取控制記錄清單。</span><span class="sxs-lookup"><span data-stu-id="65247-123">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65247-124">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="65247-124">-DeviceName</span></span>
<span data-ttu-id="65247-125">指定要更新卷的 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="65247-125">Specifies the name of the StorSimple device on which to update the volume exists.</span></span>

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

### <span data-ttu-id="65247-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="65247-126">-InformationAction</span></span>
<span data-ttu-id="65247-127">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="65247-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="65247-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="65247-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="65247-129">持續</span><span class="sxs-lookup"><span data-stu-id="65247-129">Continue</span></span>
- <span data-ttu-id="65247-130">理會</span><span class="sxs-lookup"><span data-stu-id="65247-130">Ignore</span></span>
- <span data-ttu-id="65247-131">看</span><span class="sxs-lookup"><span data-stu-id="65247-131">Inquire</span></span>
- <span data-ttu-id="65247-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="65247-132">SilentlyContinue</span></span>
- <span data-ttu-id="65247-133">停止</span><span class="sxs-lookup"><span data-stu-id="65247-133">Stop</span></span>
- <span data-ttu-id="65247-134">封存</span><span class="sxs-lookup"><span data-stu-id="65247-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65247-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="65247-135">-InformationVariable</span></span>
<span data-ttu-id="65247-136">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="65247-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65247-137">-NewName</span><span class="sxs-lookup"><span data-stu-id="65247-137">-NewName</span></span>
<span data-ttu-id="65247-138">指定 StorSimple 裝置的新名稱。</span><span class="sxs-lookup"><span data-stu-id="65247-138">Specifies a new name for the StorSimple device.</span></span>

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

### <span data-ttu-id="65247-139">-線上</span><span class="sxs-lookup"><span data-stu-id="65247-139">-Online</span></span>
<span data-ttu-id="65247-140">指定音量是否為線上。</span><span class="sxs-lookup"><span data-stu-id="65247-140">Specifies whether the volume is online.</span></span>

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

### <span data-ttu-id="65247-141">-設定檔</span><span class="sxs-lookup"><span data-stu-id="65247-141">-Profile</span></span>
<span data-ttu-id="65247-142">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="65247-142">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="65247-143">-Volume</span><span class="sxs-lookup"><span data-stu-id="65247-143">-Volume</span></span>
<span data-ttu-id="65247-144">指定要更新的卷名。</span><span class="sxs-lookup"><span data-stu-id="65247-144">Specifies the name of the volume to update.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65247-145">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="65247-145">-VolumeAppType</span></span>
<span data-ttu-id="65247-146">指定是否要將卷更新為主要或封存磁片卷。</span><span class="sxs-lookup"><span data-stu-id="65247-146">Specifies whether to update the volume to be a primary or archive volume.</span></span>
<span data-ttu-id="65247-147">有效值為： PrimaryVolume 和 ArchiveVolume。</span><span class="sxs-lookup"><span data-stu-id="65247-147">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65247-148">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="65247-148">-VolumeName</span></span>
<span data-ttu-id="65247-149">指定要更新的卷名。</span><span class="sxs-lookup"><span data-stu-id="65247-149">Specifies the name of the volume to update.</span></span>

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

### <span data-ttu-id="65247-150">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="65247-150">-VolumeSizeInBytes</span></span>
<span data-ttu-id="65247-151">指定卷的更新大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="65247-151">Specifies the updated size, in bytes, for the volume.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65247-152">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="65247-152">-WaitForComplete</span></span>
<span data-ttu-id="65247-153">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="65247-153">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="65247-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65247-154">CommonParameters</span></span>
<span data-ttu-id="65247-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65247-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65247-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65247-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65247-157">輸入</span><span class="sxs-lookup"><span data-stu-id="65247-157">INPUTS</span></span>

### <span data-ttu-id="65247-158">清單\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="65247-158">List\<AccessControlRecord\></span></span>
<span data-ttu-id="65247-159">這個 Cmdlet 接受 **AccessControlRecord** 物件的清單，以與一個卷建立關聯。</span><span class="sxs-lookup"><span data-stu-id="65247-159">This cmdlet accepts a list of **AccessControlRecord** objects to associate to a volume.</span></span>

## <span data-ttu-id="65247-160">輸出</span><span class="sxs-lookup"><span data-stu-id="65247-160">OUTPUTS</span></span>

### <span data-ttu-id="65247-161">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="65247-161">TaskStatusInfo</span></span>
<span data-ttu-id="65247-162">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="65247-162">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="65247-163">筆記</span><span class="sxs-lookup"><span data-stu-id="65247-163">NOTES</span></span>

## <span data-ttu-id="65247-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="65247-164">RELATED LINKS</span></span>

[<span data-ttu-id="65247-165">AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="65247-165">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="65247-166">新-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="65247-166">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="65247-167">移除-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="65247-167">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="65247-168">AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="65247-168">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="65247-169">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="65247-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


