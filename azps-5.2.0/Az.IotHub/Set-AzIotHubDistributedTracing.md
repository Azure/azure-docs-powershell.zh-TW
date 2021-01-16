---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281014"
---
# <span data-ttu-id="3da54-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="3da54-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="3da54-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3da54-102">SYNOPSIS</span></span>
<span data-ttu-id="3da54-103">更新裝置的分散式追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="3da54-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="3da54-104">句法</span><span class="sxs-lookup"><span data-stu-id="3da54-104">SYNTAX</span></span>

### <span data-ttu-id="3da54-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3da54-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3da54-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3da54-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3da54-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3da54-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3da54-108">說明</span><span class="sxs-lookup"><span data-stu-id="3da54-108">DESCRIPTION</span></span>
<span data-ttu-id="3da54-109">更新裝置的分散式追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="3da54-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="3da54-110">示例</span><span class="sxs-lookup"><span data-stu-id="3da54-110">EXAMPLES</span></span>

### <span data-ttu-id="3da54-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3da54-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="3da54-112">更新裝置的分散式追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="3da54-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="3da54-113">參數</span><span class="sxs-lookup"><span data-stu-id="3da54-113">PARAMETERS</span></span>

### <span data-ttu-id="3da54-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da54-114">-DefaultProfile</span></span>
<span data-ttu-id="3da54-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3da54-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3da54-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="3da54-116">-DeviceId</span></span>
<span data-ttu-id="3da54-117">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="3da54-117">Target Device Id.</span></span>

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

### <span data-ttu-id="3da54-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3da54-118">-InputObject</span></span>
<span data-ttu-id="3da54-119">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="3da54-119">IotHub object</span></span>

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

### <span data-ttu-id="3da54-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3da54-120">-IotHubName</span></span>
<span data-ttu-id="3da54-121">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="3da54-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3da54-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3da54-122">-ResourceGroupName</span></span>
<span data-ttu-id="3da54-123">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="3da54-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3da54-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3da54-124">-ResourceId</span></span>
<span data-ttu-id="3da54-125">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3da54-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3da54-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="3da54-126">-SamplingMode</span></span>
<span data-ttu-id="3da54-127">開啟分散式追蹤啟用和停用的採樣。</span><span class="sxs-lookup"><span data-stu-id="3da54-127">Turns sampling for distributed tracing enable and disable.</span></span>

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

### <span data-ttu-id="3da54-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="3da54-128">-SamplingRate</span></span>
<span data-ttu-id="3da54-129">控制加入追蹤內容所抽樣的訊息數量。</span><span class="sxs-lookup"><span data-stu-id="3da54-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="3da54-130">此值為百分比。</span><span class="sxs-lookup"><span data-stu-id="3da54-130">This value is a percentage.</span></span>
<span data-ttu-id="3da54-131">只允許從0到 100 (包含) 的值。</span><span class="sxs-lookup"><span data-stu-id="3da54-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

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

### <span data-ttu-id="3da54-132">-確認</span><span class="sxs-lookup"><span data-stu-id="3da54-132">-Confirm</span></span>
<span data-ttu-id="3da54-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3da54-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3da54-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3da54-134">-WhatIf</span></span>
<span data-ttu-id="3da54-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3da54-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3da54-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3da54-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3da54-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da54-137">CommonParameters</span></span>
<span data-ttu-id="3da54-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3da54-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da54-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3da54-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da54-140">輸入</span><span class="sxs-lookup"><span data-stu-id="3da54-140">INPUTS</span></span>

### <span data-ttu-id="3da54-141">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="3da54-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3da54-142">System.object</span><span class="sxs-lookup"><span data-stu-id="3da54-142">System.String</span></span>

## <span data-ttu-id="3da54-143">輸出</span><span class="sxs-lookup"><span data-stu-id="3da54-143">OUTPUTS</span></span>

### <span data-ttu-id="3da54-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="3da54-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="3da54-145">筆記</span><span class="sxs-lookup"><span data-stu-id="3da54-145">NOTES</span></span>

## <span data-ttu-id="3da54-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="3da54-146">RELATED LINKS</span></span>
