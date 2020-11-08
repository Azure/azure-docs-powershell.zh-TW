---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: f5463015b93c209c6cf8952c566e9656da2fba18
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136775"
---
# <span data-ttu-id="22199-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="22199-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="22199-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22199-102">SYNOPSIS</span></span>
<span data-ttu-id="22199-103">刪除 IoT Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="22199-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="22199-104">句法</span><span class="sxs-lookup"><span data-stu-id="22199-104">SYNTAX</span></span>

### <span data-ttu-id="22199-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="22199-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22199-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="22199-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22199-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="22199-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22199-108">說明</span><span class="sxs-lookup"><span data-stu-id="22199-108">DESCRIPTION</span></span>
<span data-ttu-id="22199-109">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring 。</span><span class="sxs-lookup"><span data-stu-id="22199-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="22199-110">示例</span><span class="sxs-lookup"><span data-stu-id="22199-110">EXAMPLES</span></span>

### <span data-ttu-id="22199-111">範例1</span><span class="sxs-lookup"><span data-stu-id="22199-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="22199-112">刪除 IoT Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="22199-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="22199-113">參數</span><span class="sxs-lookup"><span data-stu-id="22199-113">PARAMETERS</span></span>

### <span data-ttu-id="22199-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22199-114">-DefaultProfile</span></span>
<span data-ttu-id="22199-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22199-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22199-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22199-116">-InputObject</span></span>
<span data-ttu-id="22199-117">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="22199-117">IotHub object</span></span>

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

### <span data-ttu-id="22199-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="22199-118">-IotHubName</span></span>
<span data-ttu-id="22199-119">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="22199-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="22199-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="22199-120">-Name</span></span>
<span data-ttu-id="22199-121">部署的識別碼。</span><span class="sxs-lookup"><span data-stu-id="22199-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="22199-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22199-122">-PassThru</span></span>
<span data-ttu-id="22199-123">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="22199-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="22199-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="22199-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="22199-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22199-125">-ResourceGroupName</span></span>
<span data-ttu-id="22199-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="22199-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="22199-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22199-127">-ResourceId</span></span>
<span data-ttu-id="22199-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="22199-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="22199-129">-確認</span><span class="sxs-lookup"><span data-stu-id="22199-129">-Confirm</span></span>
<span data-ttu-id="22199-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="22199-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22199-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22199-131">-WhatIf</span></span>
<span data-ttu-id="22199-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22199-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22199-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22199-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22199-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22199-134">CommonParameters</span></span>
<span data-ttu-id="22199-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22199-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22199-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22199-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22199-137">輸入</span><span class="sxs-lookup"><span data-stu-id="22199-137">INPUTS</span></span>

### <span data-ttu-id="22199-138">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="22199-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="22199-139">System.object</span><span class="sxs-lookup"><span data-stu-id="22199-139">System.String</span></span>

## <span data-ttu-id="22199-140">輸出</span><span class="sxs-lookup"><span data-stu-id="22199-140">OUTPUTS</span></span>

### <span data-ttu-id="22199-141">System.object</span><span class="sxs-lookup"><span data-stu-id="22199-141">System.Boolean</span></span>

## <span data-ttu-id="22199-142">筆記</span><span class="sxs-lookup"><span data-stu-id="22199-142">NOTES</span></span>

## <span data-ttu-id="22199-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="22199-143">RELATED LINKS</span></span>