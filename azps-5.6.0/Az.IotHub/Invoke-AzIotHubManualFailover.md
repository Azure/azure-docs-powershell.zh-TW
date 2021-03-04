---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: f9372a246e16e719db60f52922a8a416f3de10c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906625"
---
# <span data-ttu-id="7ca97-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="7ca97-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="7ca97-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7ca97-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca97-103">針對地理位置成對的災害復原區域，為 IoT 中樞啟動容錯移轉程式。</span><span class="sxs-lookup"><span data-stu-id="7ca97-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="7ca97-104">語法</span><span class="sxs-lookup"><span data-stu-id="7ca97-104">SYNTAX</span></span>

### <span data-ttu-id="7ca97-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7ca97-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca97-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7ca97-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca97-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7ca97-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ca97-108">描述</span><span class="sxs-lookup"><span data-stu-id="7ca97-108">DESCRIPTION</span></span>
<span data-ttu-id="7ca97-109">它會觸發您的 IoT 中樞容錯移轉至次要位置。</span><span class="sxs-lookup"><span data-stu-id="7ca97-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="7ca97-110">此動作會導致解決方案的時間和遙測遺失。</span><span class="sxs-lookup"><span data-stu-id="7ca97-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="7ca97-111">這是一項長時間執行的操作，可能需要數分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="7ca97-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="7ca97-112">使用時請小心運動。</span><span class="sxs-lookup"><span data-stu-id="7ca97-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="7ca97-113">例子</span><span class="sxs-lookup"><span data-stu-id="7ca97-113">EXAMPLES</span></span>

### <span data-ttu-id="7ca97-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="7ca97-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="7ca97-115">啟動「myiothub」IoT 中樞的容錯移轉程式。</span><span class="sxs-lookup"><span data-stu-id="7ca97-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="7ca97-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="7ca97-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="7ca97-117">啟動背景中「myiothub」IoT 中樞的容錯移轉程式。</span><span class="sxs-lookup"><span data-stu-id="7ca97-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="7ca97-118">參數</span><span class="sxs-lookup"><span data-stu-id="7ca97-118">PARAMETERS</span></span>

### <span data-ttu-id="7ca97-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ca97-119">-AsJob</span></span>
<span data-ttu-id="7ca97-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ca97-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca97-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca97-121">-DefaultProfile</span></span>
<span data-ttu-id="7ca97-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ca97-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ca97-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ca97-123">-InputObject</span></span>
<span data-ttu-id="7ca97-124">Iot Hub 物件</span><span class="sxs-lookup"><span data-stu-id="7ca97-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="7ca97-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ca97-125">-Name</span></span>
<span data-ttu-id="7ca97-126">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="7ca97-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7ca97-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ca97-127">-PassThru</span></span>
<span data-ttu-id="7ca97-128">允許返回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="7ca97-128">Allows to return the boolean object.</span></span> <span data-ttu-id="7ca97-129">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7ca97-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca97-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca97-130">-ResourceGroupName</span></span>
<span data-ttu-id="7ca97-131">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="7ca97-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7ca97-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ca97-132">-ResourceId</span></span>
<span data-ttu-id="7ca97-133">Iot Hub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7ca97-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="7ca97-134">-確認</span><span class="sxs-lookup"><span data-stu-id="7ca97-134">-Confirm</span></span>
<span data-ttu-id="7ca97-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7ca97-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ca97-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ca97-136">-WhatIf</span></span>
<span data-ttu-id="7ca97-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7ca97-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ca97-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ca97-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ca97-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca97-139">CommonParameters</span></span>
<span data-ttu-id="7ca97-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7ca97-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca97-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7ca97-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca97-142">輸入</span><span class="sxs-lookup"><span data-stu-id="7ca97-142">INPUTS</span></span>

### <span data-ttu-id="7ca97-143">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7ca97-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7ca97-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7ca97-144">System.String</span></span>

## <span data-ttu-id="7ca97-145">輸出</span><span class="sxs-lookup"><span data-stu-id="7ca97-145">OUTPUTS</span></span>

### <span data-ttu-id="7ca97-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7ca97-146">System.Boolean</span></span>

## <span data-ttu-id="7ca97-147">筆記</span><span class="sxs-lookup"><span data-stu-id="7ca97-147">NOTES</span></span>

## <span data-ttu-id="7ca97-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ca97-148">RELATED LINKS</span></span>
