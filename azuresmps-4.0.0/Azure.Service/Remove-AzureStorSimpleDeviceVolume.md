---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A62D1A9D-C0EF-4305-B1F9-3AE68A79222D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a5023abffae6bbc2b70b7400e604ffabb1d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967906"
---
# <span data-ttu-id="dda72-101">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="dda72-101">Remove-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="dda72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dda72-102">SYNOPSIS</span></span>
<span data-ttu-id="dda72-103">從 StorSimple 裝置移除磁片。</span><span class="sxs-lookup"><span data-stu-id="dda72-103">Removes a volume from a StorSimple device.</span></span>

## <span data-ttu-id="dda72-104">句法</span><span class="sxs-lookup"><span data-stu-id="dda72-104">SYNTAX</span></span>

### <span data-ttu-id="dda72-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="dda72-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="dda72-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="dda72-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dda72-107">說明</span><span class="sxs-lookup"><span data-stu-id="dda72-107">DESCRIPTION</span></span>
<span data-ttu-id="dda72-108">**AzureStorSimpleDeviceVolume** Cmdlet 會從 StorSimple 裝置中移除磁片。</span><span class="sxs-lookup"><span data-stu-id="dda72-108">The **Remove-AzureStorSimpleDeviceVolume** cmdlet removes a volume from a StorSimple device.</span></span>
<span data-ttu-id="dda72-109">除非您指定 *Force* 參數，否則此 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dda72-109">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="dda72-110">示例</span><span class="sxs-lookup"><span data-stu-id="dda72-110">EXAMPLES</span></span>

### <span data-ttu-id="dda72-111">範例1：使用管線移除體積塊</span><span class="sxs-lookup"><span data-stu-id="dda72-111">Example 1: Remove a volume by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" | Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: 2933e24d-9564-42b5-9053-5f0bc4f59ea8_PS
VERBOSE: ClientRequestId: 7c2d854b-537a-4253-bb0c-c15bc8aa2b49_PS
VERBOSE: ClientRequestId: 4bf749ac-517c-49e7-8027-a8f62e272014_PS
VERBOSE: ClientRequestId: 7d9ec87a-616d-4ca9-bfb8-158859174d59_PS

Confirm
Are you sure you want to remove the volume? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 67a38e28-a015-44b1-8159-c1a6604f4d81_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: 56101c10-07ca-40f4-8f19-c6fdd895e3a5_PS
32925451-4451-4478-89f7-d8930505d3fb
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
32925451-4451-4478-89f7-d8930505d3fb for tracking the task's status
VERBOSE: Volume with name: Volume18 is found.
```

<span data-ttu-id="dda72-112">這個命令會在名為 Contoso63-AppVm 的裝置上取得名為 Volume18 的卷，然後使用管線運算子將該卷傳至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dda72-112">This command gets the volume named Volume18 on the device named Contoso63-AppVm, and then passes that volume to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dda72-113">目前的 Cmdlet 會啟動移除該卷的工作，然後傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="dda72-113">The current cmdlet starts the task that removes the volume, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="dda72-114">若要查看任務的狀態，請使用 **AzureStorSimpleTask** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dda72-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="dda72-115">此命令不會指定 *Force* 參數，因此 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dda72-115">The command does not specify the *Force* parameter, so the cmdlet prompts you for confirmation.</span></span>

### <span data-ttu-id="dda72-116">範例2：移除無確認的卷</span><span class="sxs-lookup"><span data-stu-id="dda72-116">Example 2: Remove a volume without confirmation</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Force
VERBOSE: ClientRequestId: 72f13290-41eb-4ac4-9535-da1a42d0fa0b_PS
VERBOSE: ClientRequestId: ae0c1d99-1a66-4a69-9260-f2c8c12546bd_PS
VERBOSE: ClientRequestId: 9610744f-d031-488f-87e6-3ecddb305e13_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: d33525d8-7276-4d2a-942d-d10f8078f1f7_PS
483f8cb4-ebc3-46a9-a9e6-0989e25738a0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
483f8cb4-ebc3-46a9-a9e6-0989e25738a0 for tracking the task's status
```

<span data-ttu-id="dda72-117">這個命令會從名為 Contoso63-AppVm 的裝置中移除名為 Volume18 的卷名。</span><span class="sxs-lookup"><span data-stu-id="dda72-117">This command removes the volume named Volume18 from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="dda72-118">命令會指定 *Force* 參數，因此 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dda72-118">The command specifies the *Force* parameter, so the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="dda72-119">參數</span><span class="sxs-lookup"><span data-stu-id="dda72-119">PARAMETERS</span></span>

### <span data-ttu-id="dda72-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="dda72-120">-DeviceName</span></span>
<span data-ttu-id="dda72-121">指定要移除的磁片卷名存在的 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="dda72-121">Specifies the name of the StorSimple device on which to the volume to remove exists.</span></span>

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

### <span data-ttu-id="dda72-122">-Force</span><span class="sxs-lookup"><span data-stu-id="dda72-122">-Force</span></span>
<span data-ttu-id="dda72-123">表示此 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dda72-123">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="dda72-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="dda72-124">-Profile</span></span>
<span data-ttu-id="dda72-125">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="dda72-125">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="dda72-126">-Volume</span><span class="sxs-lookup"><span data-stu-id="dda72-126">-Volume</span></span>
<span data-ttu-id="dda72-127">指定要移除的卷（ **VirtualDisk** 物件）。</span><span class="sxs-lookup"><span data-stu-id="dda72-127">Specifies the volume to remove, as a **VirtualDisk** object.</span></span>
<span data-ttu-id="dda72-128">若要取得 **VirtualDisk** 物件，請使用 **AzureStorSimpleDeviceVolume** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dda72-128">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

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

### <span data-ttu-id="dda72-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="dda72-129">-VolumeName</span></span>
<span data-ttu-id="dda72-130">指定要移除的卷名。</span><span class="sxs-lookup"><span data-stu-id="dda72-130">Specifies the name of the volume to remove.</span></span>

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

### <span data-ttu-id="dda72-131">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="dda72-131">-WaitForComplete</span></span>
<span data-ttu-id="dda72-132">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="dda72-132">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="dda72-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda72-133">CommonParameters</span></span>
<span data-ttu-id="dda72-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dda72-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda72-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dda72-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda72-136">輸入</span><span class="sxs-lookup"><span data-stu-id="dda72-136">INPUTS</span></span>

### <span data-ttu-id="dda72-137">VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="dda72-137">VirtualDisk</span></span>
<span data-ttu-id="dda72-138">這個 Cmdlet 接受要刪除的 **VirtualDisk** 物件或要刪除之 **VirtualDisk** 的卷名。</span><span class="sxs-lookup"><span data-stu-id="dda72-138">This cmdlet accepts either the **VirtualDisk** object to delete or the volume name of the **VirtualDisk** to delete.</span></span>

## <span data-ttu-id="dda72-139">輸出</span><span class="sxs-lookup"><span data-stu-id="dda72-139">OUTPUTS</span></span>

### <span data-ttu-id="dda72-140">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="dda72-140">TaskStatusInfo</span></span>
<span data-ttu-id="dda72-141">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="dda72-141">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="dda72-142">筆記</span><span class="sxs-lookup"><span data-stu-id="dda72-142">NOTES</span></span>

## <span data-ttu-id="dda72-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="dda72-143">RELATED LINKS</span></span>

[<span data-ttu-id="dda72-144">AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="dda72-144">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="dda72-145">新-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="dda72-145">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="dda72-146">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="dda72-146">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="dda72-147">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="dda72-147">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


