---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: b1bdc6b5910f47fdca8e8b66ab99939945547a08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915489"
---
# <span data-ttu-id="8241f-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="8241f-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="8241f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8241f-102">SYNOPSIS</span></span>
<span data-ttu-id="8241f-103">更新裝置分散式追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="8241f-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="8241f-104">語法</span><span class="sxs-lookup"><span data-stu-id="8241f-104">SYNTAX</span></span>

### <span data-ttu-id="8241f-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8241f-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8241f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8241f-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8241f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8241f-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8241f-108">描述</span><span class="sxs-lookup"><span data-stu-id="8241f-108">DESCRIPTION</span></span>
<span data-ttu-id="8241f-109">更新裝置分散式追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="8241f-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="8241f-110">例子</span><span class="sxs-lookup"><span data-stu-id="8241f-110">EXAMPLES</span></span>

### <span data-ttu-id="8241f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="8241f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="8241f-112">更新裝置分散式追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="8241f-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="8241f-113">參數</span><span class="sxs-lookup"><span data-stu-id="8241f-113">PARAMETERS</span></span>

### <span data-ttu-id="8241f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8241f-114">-DefaultProfile</span></span>
<span data-ttu-id="8241f-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8241f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8241f-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8241f-116">-DeviceId</span></span>
<span data-ttu-id="8241f-117">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="8241f-117">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8241f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8241f-118">-InputObject</span></span>
<span data-ttu-id="8241f-119">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="8241f-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8241f-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8241f-120">-IotHubName</span></span>
<span data-ttu-id="8241f-121">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="8241f-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8241f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8241f-122">-ResourceGroupName</span></span>
<span data-ttu-id="8241f-123">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="8241f-123">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8241f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8241f-124">-ResourceId</span></span>
<span data-ttu-id="8241f-125">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8241f-125">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8241f-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="8241f-126">-SamplingMode</span></span>
<span data-ttu-id="8241f-127">啟用和停用分散式追蹤的抽樣。</span><span class="sxs-lookup"><span data-stu-id="8241f-127">Turns sampling for distributed tracing enable and disable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDistributedTracingSamplingMode
Parameter Sets: (All)
Aliases: Mode
Accepted values: Disabled, Enabled

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8241f-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="8241f-128">-SamplingRate</span></span>
<span data-ttu-id="8241f-129">控制新增追蹤上下文的範例郵件數量。</span><span class="sxs-lookup"><span data-stu-id="8241f-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="8241f-130">此值是百分比。</span><span class="sxs-lookup"><span data-stu-id="8241f-130">This value is a percentage.</span></span>
<span data-ttu-id="8241f-131">僅允許 0 到 100 (含) 的值。</span><span class="sxs-lookup"><span data-stu-id="8241f-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Rate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8241f-132">-確認</span><span class="sxs-lookup"><span data-stu-id="8241f-132">-Confirm</span></span>
<span data-ttu-id="8241f-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8241f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8241f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8241f-134">-WhatIf</span></span>
<span data-ttu-id="8241f-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8241f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8241f-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8241f-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8241f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8241f-137">CommonParameters</span></span>
<span data-ttu-id="8241f-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8241f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8241f-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8241f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8241f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="8241f-140">INPUTS</span></span>

### <span data-ttu-id="8241f-141">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8241f-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8241f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8241f-142">System.String</span></span>

## <span data-ttu-id="8241f-143">輸出</span><span class="sxs-lookup"><span data-stu-id="8241f-143">OUTPUTS</span></span>

### <span data-ttu-id="8241f-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDMicrosoft.Azure.Commands.Management.IotHub.Models.PSD追蹤</span><span class="sxs-lookup"><span data-stu-id="8241f-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="8241f-145">筆記</span><span class="sxs-lookup"><span data-stu-id="8241f-145">NOTES</span></span>

## <span data-ttu-id="8241f-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="8241f-146">RELATED LINKS</span></span>
