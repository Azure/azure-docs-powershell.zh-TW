---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 3451c9d1553a22e33b1aa56f2318c8f831e16468
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906622"
---
# <span data-ttu-id="b1e32-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1e32-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="b1e32-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b1e32-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e32-103">刪除 IoT 裝置組配置。</span><span class="sxs-lookup"><span data-stu-id="b1e32-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="b1e32-104">語法</span><span class="sxs-lookup"><span data-stu-id="b1e32-104">SYNTAX</span></span>

### <span data-ttu-id="b1e32-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b1e32-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1e32-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b1e32-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1e32-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b1e32-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1e32-108">描述</span><span class="sxs-lookup"><span data-stu-id="b1e32-108">DESCRIPTION</span></span>
<span data-ttu-id="b1e32-109">請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b1e32-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="b1e32-110">例子</span><span class="sxs-lookup"><span data-stu-id="b1e32-110">EXAMPLES</span></span>

### <span data-ttu-id="b1e32-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b1e32-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="b1e32-112">刪除 IoT 裝置組配置。</span><span class="sxs-lookup"><span data-stu-id="b1e32-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="b1e32-113">參數</span><span class="sxs-lookup"><span data-stu-id="b1e32-113">PARAMETERS</span></span>

### <span data-ttu-id="b1e32-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1e32-114">-DefaultProfile</span></span>
<span data-ttu-id="b1e32-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1e32-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1e32-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1e32-116">-InputObject</span></span>
<span data-ttu-id="b1e32-117">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="b1e32-117">IotHub object</span></span>

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

### <span data-ttu-id="b1e32-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b1e32-118">-IotHubName</span></span>
<span data-ttu-id="b1e32-119">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="b1e32-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b1e32-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1e32-120">-Name</span></span>
<span data-ttu-id="b1e32-121">組配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1e32-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="b1e32-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1e32-122">-PassThru</span></span>
<span data-ttu-id="b1e32-123">允許返回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="b1e32-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="b1e32-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b1e32-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1e32-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1e32-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1e32-126">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="b1e32-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b1e32-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1e32-127">-ResourceId</span></span>
<span data-ttu-id="b1e32-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b1e32-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b1e32-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b1e32-129">-Confirm</span></span>
<span data-ttu-id="b1e32-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b1e32-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1e32-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1e32-131">-WhatIf</span></span>
<span data-ttu-id="b1e32-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1e32-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1e32-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1e32-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1e32-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e32-134">CommonParameters</span></span>
<span data-ttu-id="b1e32-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b1e32-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e32-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b1e32-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e32-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b1e32-137">INPUTS</span></span>

### <span data-ttu-id="b1e32-138">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b1e32-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b1e32-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b1e32-139">System.String</span></span>

## <span data-ttu-id="b1e32-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b1e32-140">OUTPUTS</span></span>

### <span data-ttu-id="b1e32-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1e32-141">System.Boolean</span></span>

## <span data-ttu-id="b1e32-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b1e32-142">NOTES</span></span>

## <span data-ttu-id="b1e32-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1e32-143">RELATED LINKS</span></span>
