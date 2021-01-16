---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98289072"
---
# <span data-ttu-id="bb354-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="bb354-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="bb354-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb354-102">SYNOPSIS</span></span>
<span data-ttu-id="bb354-103">刪除 IoT 中樞裝置。</span><span class="sxs-lookup"><span data-stu-id="bb354-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="bb354-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb354-104">SYNTAX</span></span>

### <span data-ttu-id="bb354-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bb354-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb354-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb354-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb354-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bb354-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb354-108">說明</span><span class="sxs-lookup"><span data-stu-id="bb354-108">DESCRIPTION</span></span>
<span data-ttu-id="bb354-109">從 Iot 中樞刪除所有裝置或特定裝置。</span><span class="sxs-lookup"><span data-stu-id="bb354-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="bb354-110">示例</span><span class="sxs-lookup"><span data-stu-id="bb354-110">EXAMPLES</span></span>

### <span data-ttu-id="bb354-111">範例1</span><span class="sxs-lookup"><span data-stu-id="bb354-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="bb354-112">刪除所有的 Iot 中樞裝置。</span><span class="sxs-lookup"><span data-stu-id="bb354-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="bb354-113">範例2</span><span class="sxs-lookup"><span data-stu-id="bb354-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="bb354-114">刪除 Iot 中樞裝置。</span><span class="sxs-lookup"><span data-stu-id="bb354-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="bb354-115">參數</span><span class="sxs-lookup"><span data-stu-id="bb354-115">PARAMETERS</span></span>

### <span data-ttu-id="bb354-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb354-116">-DefaultProfile</span></span>
<span data-ttu-id="bb354-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb354-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb354-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="bb354-118">-DeviceId</span></span>
<span data-ttu-id="bb354-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb354-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb354-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb354-120">-InputObject</span></span>
<span data-ttu-id="bb354-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="bb354-121">IotHub object</span></span>

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

### <span data-ttu-id="bb354-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="bb354-122">-IotHubName</span></span>
<span data-ttu-id="bb354-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="bb354-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bb354-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb354-124">-PassThru</span></span>
<span data-ttu-id="bb354-125">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="bb354-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="bb354-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="bb354-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bb354-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb354-127">-ResourceGroupName</span></span>
<span data-ttu-id="bb354-128">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="bb354-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bb354-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb354-129">-ResourceId</span></span>
<span data-ttu-id="bb354-130">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bb354-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="bb354-131">-確認</span><span class="sxs-lookup"><span data-stu-id="bb354-131">-Confirm</span></span>
<span data-ttu-id="bb354-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bb354-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb354-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb354-133">-WhatIf</span></span>
<span data-ttu-id="bb354-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb354-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb354-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb354-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb354-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb354-136">CommonParameters</span></span>
<span data-ttu-id="bb354-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb354-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb354-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb354-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb354-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bb354-139">INPUTS</span></span>

### <span data-ttu-id="bb354-140">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="bb354-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="bb354-141">System.object</span><span class="sxs-lookup"><span data-stu-id="bb354-141">System.String</span></span>

## <span data-ttu-id="bb354-142">輸出</span><span class="sxs-lookup"><span data-stu-id="bb354-142">OUTPUTS</span></span>

### <span data-ttu-id="bb354-143">System.object</span><span class="sxs-lookup"><span data-stu-id="bb354-143">System.Boolean</span></span>

## <span data-ttu-id="bb354-144">筆記</span><span class="sxs-lookup"><span data-stu-id="bb354-144">NOTES</span></span>

## <span data-ttu-id="bb354-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb354-145">RELATED LINKS</span></span>
