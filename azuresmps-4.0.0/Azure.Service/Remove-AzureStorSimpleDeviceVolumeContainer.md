---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C50959BB-7481-4898-BF4B-C5ABF8758473
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2c06455004afbd15235f59164034abc2147964b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967899"
---
# <span data-ttu-id="73ce8-101">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="73ce8-101">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="73ce8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="73ce8-103">從 StorSimple 裝置移除卷容器。</span><span class="sxs-lookup"><span data-stu-id="73ce8-103">Removes a volume container from a StorSimple device.</span></span>

## <span data-ttu-id="73ce8-104">句法</span><span class="sxs-lookup"><span data-stu-id="73ce8-104">SYNTAX</span></span>

```
Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainer <DataContainer>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="73ce8-105">說明</span><span class="sxs-lookup"><span data-stu-id="73ce8-105">DESCRIPTION</span></span>
<span data-ttu-id="73ce8-106">**AzureStorSimpleDeviceVolumeContainer** Cmdlet 會從 StorSimple 裝置中移除卷容器物件。</span><span class="sxs-lookup"><span data-stu-id="73ce8-106">The **Remove-AzureStorSimpleDeviceVolumeContainer** cmdlet removes a volume container object from a StorSimple device.</span></span>
<span data-ttu-id="73ce8-107">除非您指定 *Force* 參數，否則此 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73ce8-107">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="73ce8-108">示例</span><span class="sxs-lookup"><span data-stu-id="73ce8-108">EXAMPLES</span></span>

### <span data-ttu-id="73ce8-109">範例1：使用管線移除容器</span><span class="sxs-lookup"><span data-stu-id="73ce8-109">Example 1: Remove a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" | Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -Force
VERBOSE: ClientRequestId: 0efbb4fc-ceb0-4311-bc49-0e08161d0a37_PS
VERBOSE: ClientRequestId: bf5b615f-47e3-4868-91b6-f2d12217a302_PS
VERBOSE: ClientRequestId: 5590c87e-0602-4197-b6c3-cf58b0e7a7b3_PS
VERBOSE: ClientRequestId: b33c71ac-c345-44ff-8213-d7fdf9f8480a_PS
VERBOSE: ClientRequestId: 903d42ef-58f4-4e89-ba7f-5f234262356d_PS
VERBOSE: About to create a job to remove your Volume container! 
VERBOSE: ClientRequestId: 2279575f-5115-4344-9c6f-9ef599bd203e_PS
e9ddec89-67ac-4e2e-a2ed-820de3547bb0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
e9ddec89-67ac-4e2e-a2ed-820de3547bb0 for tracking the task's status
VERBOSE: Volume container with name: Container08 is found.
```

<span data-ttu-id="73ce8-110">這個命令會使用 **AzureStorSimpleDeviceVolumeContainer** Cmdlet，在名為 Contoso63-AppVm 的裝置上取得名為 Container08 的卷容器。</span><span class="sxs-lookup"><span data-stu-id="73ce8-110">This command gets the volume container named Container08 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="73ce8-111">命令會使用管線運算子，將卷容器傳到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73ce8-111">The command passes the volume container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="73ce8-112">這個命令會啟動工作來移除容器，然後傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="73ce8-112">This command starts the task to remove the container, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="73ce8-113">若要查看任務的狀態，請使用 **AzureStorSimpleTask** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73ce8-113">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="73ce8-114">這個命令會指定 *Force* 參數，因此它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73ce8-114">This command specifies the *Force* parameter, so it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="73ce8-115">參數</span><span class="sxs-lookup"><span data-stu-id="73ce8-115">PARAMETERS</span></span>

### <span data-ttu-id="73ce8-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="73ce8-116">-DeviceName</span></span>
<span data-ttu-id="73ce8-117">指定要移除的磁片卷容器所在的 StorSimple 裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="73ce8-117">Specifies the name of the StorSimple device on which to the volume container to remove exists.</span></span>

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

### <span data-ttu-id="73ce8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="73ce8-118">-Force</span></span>
<span data-ttu-id="73ce8-119">表示此 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73ce8-119">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="73ce8-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="73ce8-120">-Profile</span></span>
<span data-ttu-id="73ce8-121">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="73ce8-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="73ce8-122">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="73ce8-122">-VolumeContainer</span></span>
<span data-ttu-id="73ce8-123">指定要移除的卷容器，做為 **DataContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="73ce8-123">Specifies the volume container to remove, as a **DataContainer** object.</span></span>
<span data-ttu-id="73ce8-124">若要取得 **DataContainer** 物件，請使用 **AzureStorSimpleDeviceVolumeContainer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73ce8-124">To obtain a **DataContainer** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73ce8-125">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="73ce8-125">-WaitForComplete</span></span>
<span data-ttu-id="73ce8-126">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="73ce8-126">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="73ce8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ce8-127">CommonParameters</span></span>
<span data-ttu-id="73ce8-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73ce8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ce8-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73ce8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ce8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="73ce8-130">INPUTS</span></span>

### <span data-ttu-id="73ce8-131">DataContainer</span><span class="sxs-lookup"><span data-stu-id="73ce8-131">DataContainer</span></span>
<span data-ttu-id="73ce8-132">這個 Cmdlet 接受要移除的 **DataContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="73ce8-132">This cmdlet accepts a **DataContainer** object to remove.</span></span>

## <span data-ttu-id="73ce8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="73ce8-133">OUTPUTS</span></span>

### <span data-ttu-id="73ce8-134">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="73ce8-134">TaskStatusInfo</span></span>
<span data-ttu-id="73ce8-135">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="73ce8-135">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="73ce8-136">筆記</span><span class="sxs-lookup"><span data-stu-id="73ce8-136">NOTES</span></span>

## <span data-ttu-id="73ce8-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="73ce8-137">RELATED LINKS</span></span>

[<span data-ttu-id="73ce8-138">AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="73ce8-138">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="73ce8-139">新-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="73ce8-139">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


