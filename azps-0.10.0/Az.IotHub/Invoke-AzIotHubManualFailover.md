---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: 5055960ae541ef93d57eee53078413143fad7839
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795606"
---
# <span data-ttu-id="c8eb9-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="c8eb9-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="c8eb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="c8eb9-103">將 IoT 中樞的容錯移轉程式喚醒至地域配對的災害復原區域。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="c8eb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8eb9-104">SYNTAX</span></span>

### <span data-ttu-id="c8eb9-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c8eb9-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8eb9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c8eb9-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8eb9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c8eb9-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8eb9-108">說明</span><span class="sxs-lookup"><span data-stu-id="c8eb9-108">DESCRIPTION</span></span>
<span data-ttu-id="c8eb9-109">它會觸發您的 IoT 中樞到次要位置的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="c8eb9-110">此動作會導致您的解決方案發生停機時間和遙測損失。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="c8eb9-111">這是長時間執行的作業，可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="c8eb9-112">使用時，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="c8eb9-113">示例</span><span class="sxs-lookup"><span data-stu-id="c8eb9-113">EXAMPLES</span></span>

### <span data-ttu-id="c8eb9-114">範例1</span><span class="sxs-lookup"><span data-stu-id="c8eb9-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="c8eb9-115">啟動「myiothub」 IoT 中樞的容錯移轉程式。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="c8eb9-116">範例2</span><span class="sxs-lookup"><span data-stu-id="c8eb9-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="c8eb9-117">在背景中啟動「myiothub」 IoT 中樞的容錯移轉程式。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="c8eb9-118">參數</span><span class="sxs-lookup"><span data-stu-id="c8eb9-118">PARAMETERS</span></span>

### <span data-ttu-id="c8eb9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8eb9-119">-AsJob</span></span>
<span data-ttu-id="c8eb9-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8eb9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8eb9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8eb9-121">-DefaultProfile</span></span>
<span data-ttu-id="c8eb9-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8eb9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8eb9-123">-InputObject</span></span>
<span data-ttu-id="c8eb9-124">Iot 中樞物件</span><span class="sxs-lookup"><span data-stu-id="c8eb9-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="c8eb9-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8eb9-125">-Name</span></span>
<span data-ttu-id="c8eb9-126">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="c8eb9-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c8eb9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8eb9-127">-PassThru</span></span>
<span data-ttu-id="c8eb9-128">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-128">Allows to return the boolean object.</span></span> <span data-ttu-id="c8eb9-129">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8eb9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8eb9-130">-ResourceGroupName</span></span>
<span data-ttu-id="c8eb9-131">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c8eb9-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c8eb9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8eb9-132">-ResourceId</span></span>
<span data-ttu-id="c8eb9-133">Iot 中心資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c8eb9-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="c8eb9-134">-確認</span><span class="sxs-lookup"><span data-stu-id="c8eb9-134">-Confirm</span></span>
<span data-ttu-id="c8eb9-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8eb9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8eb9-136">-WhatIf</span></span>
<span data-ttu-id="c8eb9-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8eb9-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8eb9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8eb9-139">CommonParameters</span></span>
<span data-ttu-id="c8eb9-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8eb9-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8eb9-142">輸入</span><span class="sxs-lookup"><span data-stu-id="c8eb9-142">INPUTS</span></span>

### <span data-ttu-id="c8eb9-143">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="c8eb9-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c8eb9-144">System.object</span><span class="sxs-lookup"><span data-stu-id="c8eb9-144">System.String</span></span>

## <span data-ttu-id="c8eb9-145">輸出</span><span class="sxs-lookup"><span data-stu-id="c8eb9-145">OUTPUTS</span></span>

### <span data-ttu-id="c8eb9-146">System.object</span><span class="sxs-lookup"><span data-stu-id="c8eb9-146">System.Boolean</span></span>

## <span data-ttu-id="c8eb9-147">筆記</span><span class="sxs-lookup"><span data-stu-id="c8eb9-147">NOTES</span></span>

## <span data-ttu-id="c8eb9-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8eb9-148">RELATED LINKS</span></span>