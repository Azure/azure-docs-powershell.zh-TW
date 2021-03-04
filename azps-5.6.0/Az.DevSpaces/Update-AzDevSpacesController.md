---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: a531ffb8a4fae50b6d352fd1167af9c13cee409c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916969"
---
# <span data-ttu-id="85c1e-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="85c1e-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="85c1e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="85c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="85c1e-103">更新 DevSpaces 控制器以新增標記。</span><span class="sxs-lookup"><span data-stu-id="85c1e-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="85c1e-104">語法</span><span class="sxs-lookup"><span data-stu-id="85c1e-104">SYNTAX</span></span>

### <span data-ttu-id="85c1e-105">DevSpacesControllerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="85c1e-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85c1e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c1e-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85c1e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c1e-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85c1e-108">描述</span><span class="sxs-lookup"><span data-stu-id="85c1e-108">DESCRIPTION</span></span>
<span data-ttu-id="85c1e-109">更新 DevSpaces 控制器以新增標記。</span><span class="sxs-lookup"><span data-stu-id="85c1e-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="85c1e-110">例子</span><span class="sxs-lookup"><span data-stu-id="85c1e-110">EXAMPLES</span></span>

### <span data-ttu-id="85c1e-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="85c1e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="85c1e-112">標記 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="85c1e-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="85c1e-113">參數</span><span class="sxs-lookup"><span data-stu-id="85c1e-113">PARAMETERS</span></span>

### <span data-ttu-id="85c1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c1e-114">-DefaultProfile</span></span>
<span data-ttu-id="85c1e-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="85c1e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85c1e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85c1e-116">-InputObject</span></span>
<span data-ttu-id="85c1e-117">PSController 物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="85c1e-117">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85c1e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="85c1e-118">-Name</span></span>
<span data-ttu-id="85c1e-119">DevSpaces 控制器名稱。</span><span class="sxs-lookup"><span data-stu-id="85c1e-119">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c1e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85c1e-120">-ResourceGroupName</span></span>
<span data-ttu-id="85c1e-121">資源組名</span><span class="sxs-lookup"><span data-stu-id="85c1e-121">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c1e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85c1e-122">-ResourceId</span></span>
<span data-ttu-id="85c1e-123">DevSpaces 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="85c1e-123">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c1e-124">-標記</span><span class="sxs-lookup"><span data-stu-id="85c1e-124">-Tag</span></span>
<span data-ttu-id="85c1e-125">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="85c1e-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c1e-126">-確認</span><span class="sxs-lookup"><span data-stu-id="85c1e-126">-Confirm</span></span>
<span data-ttu-id="85c1e-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="85c1e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85c1e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c1e-128">-WhatIf</span></span>
<span data-ttu-id="85c1e-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="85c1e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85c1e-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85c1e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85c1e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c1e-131">CommonParameters</span></span>
<span data-ttu-id="85c1e-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="85c1e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c1e-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="85c1e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c1e-134">輸入</span><span class="sxs-lookup"><span data-stu-id="85c1e-134">INPUTS</span></span>

### <span data-ttu-id="85c1e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="85c1e-135">System.String</span></span>

### <span data-ttu-id="85c1e-136">Microsoft.Azure.Commands.DevSpaces.models.PSController</span><span class="sxs-lookup"><span data-stu-id="85c1e-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="85c1e-137">輸出</span><span class="sxs-lookup"><span data-stu-id="85c1e-137">OUTPUTS</span></span>

### <span data-ttu-id="85c1e-138">Microsoft.Azure.Commands.DevSpaces.models.PSController</span><span class="sxs-lookup"><span data-stu-id="85c1e-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="85c1e-139">筆記</span><span class="sxs-lookup"><span data-stu-id="85c1e-139">NOTES</span></span>

## <span data-ttu-id="85c1e-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="85c1e-140">RELATED LINKS</span></span>
