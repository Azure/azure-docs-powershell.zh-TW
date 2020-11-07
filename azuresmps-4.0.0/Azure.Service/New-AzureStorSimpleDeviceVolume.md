---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 049201C9-590F-47EB-9030-25F80CD8DFA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f3337556a9d7bd52e5800af5cdbd65b71ab9818
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966969"
---
# <span data-ttu-id="ce1b0-101">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="ce1b0-101">New-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="ce1b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="ce1b0-103">在指定的卷容器中建立一個卷。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-103">Creates a volume in a specified volume container.</span></span>

## <span data-ttu-id="ce1b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce1b0-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer> -VolumeName <String>
 -VolumeSizeInBytes <Int64>
 -AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>
 -VolumeAppType <AppType> -Online <Boolean> -EnableDefaultBackup <Boolean> -EnableMonitoring <Boolean>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ce1b0-105">說明</span><span class="sxs-lookup"><span data-stu-id="ce1b0-105">DESCRIPTION</span></span>
<span data-ttu-id="ce1b0-106">**新的-AzureStorSimpleDeviceVolume** Cmdlet 會在指定的磁片卷容器中建立一個卷。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-106">The **New-AzureStorSimpleDeviceVolume** cmdlet creates a volume in a specified volume container.</span></span>
<span data-ttu-id="ce1b0-107">這個 Cmdlet 會將每一個卷與一個或多個存取控制記錄關聯。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-107">This cmdlet associates each volume with one or more access control records.</span></span>
<span data-ttu-id="ce1b0-108">若要取得 **AccessControlRecord** 物件，請使用 **AzureStorSimpleAccessControlRecord** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-108">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="ce1b0-109">指定卷名、大小及 AppType。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-109">Specify a name, size, and AppType for the volume.</span></span>
<span data-ttu-id="ce1b0-110">此外，您也可以指定是否要在線上建立大量磁片，是否要啟用預設備份，以及是否要啟用監視。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-110">Also, specify whether to create the volume online, whether to enable default backup, and whether to enable monitoring.</span></span>

## <span data-ttu-id="ce1b0-111">示例</span><span class="sxs-lookup"><span data-stu-id="ce1b0-111">EXAMPLES</span></span>

### <span data-ttu-id="ce1b0-112">範例1：建立體積</span><span class="sxs-lookup"><span data-stu-id="ce1b0-112">Example 1: Create a volume</span></span>
```
PS C:\>$AcrList = Get-AzureStorSimpleAccessControlRecord
PS C:\> Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer07" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Size 2000000000 -AccessControlRecords $AcrList -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False

VERBOSE: ClientRequestId: a29d1a84-1f81-4f20-9130-7adfe45e41fb_PS
VERBOSE: ClientRequestId: 8fa63df1-3f81-4029-a536-b536a70068ad_PS
VERBOSE: ClientRequestId: 964c5744-8bb1-4f70-beda-95ca4c7f3eb6_PS
VERBOSE: ClientRequestId: f09fff3a-54fa-4a0e-93db-b079260ed2dd_PS
VERBOSE: ClientRequestId: 59aa29e3-8044-411a-adae-b64a2681ffed_PS
VERBOSE: ClientRequestId: 0ffd0297-19be-40fe-a64e-6a2947d831b4_PS
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90 for tracking the task's status
VERBOSE: Volume container with name: VolumeContainer07 is found.
```

<span data-ttu-id="ce1b0-113">第一個命令會使用 **AzureStorSimpleAccessControlRecord** Cmdlet 來取得 StorSimple Manager 服務設定中的存取控制記錄，然後將它們儲存在 $AcrList 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-113">The first command gets the access control records in the StorSimple Manager service configuration by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet, and then stores them in the $AcrList variable.</span></span>

<span data-ttu-id="ce1b0-114">第二個命令會使用 **AzureStorSimpleDeviceVolumeContainer** Cmdlet，透過名為 Contoso63-AppVm 的裝置，取得名為 VolumeContainer07 的大量容器。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-114">The second command gets the volume container named VolumeContainer07 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="ce1b0-115">命令會使用管線運算子，將該容器傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-115">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ce1b0-116">這個 Cmdlet 會建立大量的磁片。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-116">This cmdlet creates the volume.</span></span>
<span data-ttu-id="ce1b0-117">命令會指定卷名、大小，以及儲存在 $AcrList 中的存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-117">The command specifies the name for the volume, the size, and the access control records stored in $AcrList.</span></span>
<span data-ttu-id="ce1b0-118">這個命令會啟動作業，然後傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-118">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="ce1b0-119">若要查看作業的狀態，請使用 **AzureStorSimpleTask** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-119">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="ce1b0-120">範例2：建立沒有 Access Controlaccess 控制項 recordsaccess 控制項的卷</span><span class="sxs-lookup"><span data-stu-id="ce1b0-120">Example 2: Create a volume without Access Controlaccess control recordsaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer01" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume22" -Size 2000000000 -AccessControlRecords @() -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False -WaitForComplete
VERBOSE: ClientRequestId: 3f359790-7e1f-48e7-acf8-ecabba850966_PS
VERBOSE: ClientRequestId: 2723ebcf-cd72-47bb-99b5-0c099d45641b_PS
VERBOSE: ClientRequestId: e605091f-dd63-42a7-bda2-24753cbc1f9a_PS
VERBOSE: ClientRequestId: b3fd08c3-67c5-4309-9591-15d92c360469_PS
VERBOSE: ClientRequestId: 15a024a3-b0c9-4f83-9c34-0ed8b95d024b_PS
VERBOSE: ClientRequestId: c13f92f9-aea1-40dd-af80-3affe273adbe_PS


TaskId       : ceef657e-390e-4f7a-aab7-669a29c29e7f
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 1d79febf-f752-4255-af2d-230d40773bc6_PS
AccessType             : NoAccess
AcrIdList              : {}
AcrList                : {}
AppType                : PrimaryVolume
DataContainer          : Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainer
DataContainerId        : 68b63d15-6aa5-4e69-9f9d-4a0bc607d6e9
InstanceId             : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd
InternalInstanceId     : 
IsBackupEnabled        : False
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
Name                   : Volume22
Online                 : True
OperationInProgress    : None
SizeInBytes            : 2000000000
VSN                    : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd

VERBOSE: Volume container with name: VolumeContainer01 is found.
```

<span data-ttu-id="ce1b0-121">這個命令會使用 **AzureStorSimpleDeviceVolumeContainer** Cmdlet，透過名為 Contoso63-AppVm 的裝置，取得名為 VolumeContainer01 的大量容器。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-121">This command gets the volume container named VolumeContainer01 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="ce1b0-122">命令會使用管線運算子，將該容器傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-122">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ce1b0-123">這個 Cmdlet 會建立大量的磁片。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-123">This cmdlet creates the volume.</span></span>
<span data-ttu-id="ce1b0-124">此命令會指定該卷的名稱、大小，以及存取控制記錄的空白值。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-124">The command specifies the name for the volume, the size, and an empty value for access control records.</span></span>
<span data-ttu-id="ce1b0-125">這個命令會指定 *WaitForComplete* 參數，因此它會在建立體積之後傳回 **TaskStatusInfo** 。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-125">This command specifies the *WaitForComplete* parameter, so it returns a **TaskStatusInfo** after it creates the volume.</span></span>

<span data-ttu-id="ce1b0-126">因為命令不會指定存取控制記錄，所以無法存取此卷。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-126">Because the command specifies no access control records, this volume cannot be accessed.</span></span>
<span data-ttu-id="ce1b0-127">您可以稍後使用 **AzureStorSimpleDeviceVolume** Cmdlet 新增 access。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-127">You can add access, later, by using **Set-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

## <span data-ttu-id="ce1b0-128">參數</span><span class="sxs-lookup"><span data-stu-id="ce1b0-128">PARAMETERS</span></span>

### <span data-ttu-id="ce1b0-129">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="ce1b0-129">-AccessControlRecords</span></span>
<span data-ttu-id="ce1b0-130">指定要與該卷建立關聯的存取控制記錄清單。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-130">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b0-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ce1b0-131">-DeviceName</span></span>
<span data-ttu-id="ce1b0-132">指定要在其上建立卷的 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-132">Specifies the name of the StorSimple device on which to create the volume.</span></span>

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

### <span data-ttu-id="ce1b0-133">-EnableDefaultBackup</span><span class="sxs-lookup"><span data-stu-id="ce1b0-133">-EnableDefaultBackup</span></span>
<span data-ttu-id="ce1b0-134">指定是否要啟用卷的預設備份。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-134">Specifies whether to enable default backup for the volume.</span></span>

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

### <span data-ttu-id="ce1b0-135">-EnableMonitoring</span><span class="sxs-lookup"><span data-stu-id="ce1b0-135">-EnableMonitoring</span></span>
<span data-ttu-id="ce1b0-136">指定是否要啟用卷的監視。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-136">Specifies whether to enable monitoring for the volume.</span></span>

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

### <span data-ttu-id="ce1b0-137">-線上</span><span class="sxs-lookup"><span data-stu-id="ce1b0-137">-Online</span></span>
<span data-ttu-id="ce1b0-138">指定是否要在線上建立大量磁片。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-138">Specifies whether to create the volume online.</span></span>

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

### <span data-ttu-id="ce1b0-139">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ce1b0-139">-Profile</span></span>
<span data-ttu-id="ce1b0-140">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-140">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ce1b0-141">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="ce1b0-141">-VolumeAppType</span></span>
<span data-ttu-id="ce1b0-142">指定是否要建立主要或封存檔量。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-142">Specifies whether to create a primary or archive volume.</span></span>
<span data-ttu-id="ce1b0-143">有效值為： PrimaryVolume 和 ArchiveVolume。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-143">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b0-144">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="ce1b0-144">-VolumeContainer</span></span>
<span data-ttu-id="ce1b0-145">指定要在其中建立卷的 **DataContainer** 物件作為容器。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-145">Specifies the container, as a **DataContainer** object, in which to create the volume.</span></span>
<span data-ttu-id="ce1b0-146">若要取得 **VirtualDisk** 物件，請使用 **AzureStorSimpleDeviceVolumeContainer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-146">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b0-147">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="ce1b0-147">-VolumeName</span></span>
<span data-ttu-id="ce1b0-148">指定新卷的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-148">Specifies a name for the new volume.</span></span>

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

### <span data-ttu-id="ce1b0-149">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="ce1b0-149">-VolumeSizeInBytes</span></span>
<span data-ttu-id="ce1b0-150">指定音量大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-150">Specifies the volume size in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b0-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="ce1b0-151">-WaitForComplete</span></span>
<span data-ttu-id="ce1b0-152">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-152">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="ce1b0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce1b0-153">CommonParameters</span></span>
<span data-ttu-id="ce1b0-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce1b0-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce1b0-156">輸入</span><span class="sxs-lookup"><span data-stu-id="ce1b0-156">INPUTS</span></span>

### <span data-ttu-id="ce1b0-157">DataContainer、清單\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="ce1b0-157">DataContainer, List\<AccessControlRecord\></span></span>
<span data-ttu-id="ce1b0-158">這個 Cmdlet 接受 **DataContainer** 物件以及新卷的 **AccessControlRecord** 物件清單。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-158">This cmdlet accepts a **DataContainer** object and a list of **AccessControlRecord** objects for the new volume.</span></span>

## <span data-ttu-id="ce1b0-159">輸出</span><span class="sxs-lookup"><span data-stu-id="ce1b0-159">OUTPUTS</span></span>

### <span data-ttu-id="ce1b0-160">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="ce1b0-160">TaskStatusInfo</span></span>
<span data-ttu-id="ce1b0-161">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="ce1b0-161">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="ce1b0-162">筆記</span><span class="sxs-lookup"><span data-stu-id="ce1b0-162">NOTES</span></span>

## <span data-ttu-id="ce1b0-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce1b0-163">RELATED LINKS</span></span>

[<span data-ttu-id="ce1b0-164">AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="ce1b0-164">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="ce1b0-165">移除-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="ce1b0-165">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="ce1b0-166">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="ce1b0-166">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="ce1b0-167">AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ce1b0-167">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="ce1b0-168">AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="ce1b0-168">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="ce1b0-169">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="ce1b0-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


