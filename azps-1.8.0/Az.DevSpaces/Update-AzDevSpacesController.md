---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 2a94d74fb8c6ba6cc9f6c2873269f3009c2f7e9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622406"
---
# <span data-ttu-id="6ba30-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="6ba30-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="6ba30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ba30-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba30-103">更新 DevSpaces 控制器以新增標記。</span><span class="sxs-lookup"><span data-stu-id="6ba30-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="6ba30-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ba30-104">SYNTAX</span></span>

### <span data-ttu-id="6ba30-105">DevSpacesControllerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6ba30-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba30-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba30-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba30-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba30-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ba30-108">說明</span><span class="sxs-lookup"><span data-stu-id="6ba30-108">DESCRIPTION</span></span>
<span data-ttu-id="6ba30-109">更新 DevSpaces 控制器以新增標記。</span><span class="sxs-lookup"><span data-stu-id="6ba30-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="6ba30-110">示例</span><span class="sxs-lookup"><span data-stu-id="6ba30-110">EXAMPLES</span></span>

### <span data-ttu-id="6ba30-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6ba30-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="6ba30-112">標記 DevSpaces contoller。</span><span class="sxs-lookup"><span data-stu-id="6ba30-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="6ba30-113">參數</span><span class="sxs-lookup"><span data-stu-id="6ba30-113">PARAMETERS</span></span>

### <span data-ttu-id="6ba30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba30-114">-DefaultProfile</span></span>
<span data-ttu-id="6ba30-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ba30-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ba30-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ba30-116">-InputObject</span></span>
<span data-ttu-id="6ba30-117">PSController 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6ba30-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6ba30-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ba30-118">-Name</span></span>
<span data-ttu-id="6ba30-119">DevSpaces 控制器名稱。</span><span class="sxs-lookup"><span data-stu-id="6ba30-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="6ba30-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ba30-120">-ResourceGroupName</span></span>
<span data-ttu-id="6ba30-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="6ba30-121">Resource group name</span></span>

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

### <span data-ttu-id="6ba30-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ba30-122">-ResourceId</span></span>
<span data-ttu-id="6ba30-123">DevSpaces 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6ba30-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="6ba30-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ba30-124">-Tag</span></span>
<span data-ttu-id="6ba30-125">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6ba30-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="6ba30-126">-確認</span><span class="sxs-lookup"><span data-stu-id="6ba30-126">-Confirm</span></span>
<span data-ttu-id="6ba30-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ba30-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ba30-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ba30-128">-WhatIf</span></span>
<span data-ttu-id="6ba30-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ba30-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ba30-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ba30-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ba30-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba30-131">CommonParameters</span></span>
<span data-ttu-id="6ba30-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ba30-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba30-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ba30-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba30-134">輸入</span><span class="sxs-lookup"><span data-stu-id="6ba30-134">INPUTS</span></span>

### <span data-ttu-id="6ba30-135">System.object</span><span class="sxs-lookup"><span data-stu-id="6ba30-135">System.String</span></span>

### <span data-ttu-id="6ba30-136">PSController 中的 DevSpaces。</span><span class="sxs-lookup"><span data-stu-id="6ba30-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="6ba30-137">輸出</span><span class="sxs-lookup"><span data-stu-id="6ba30-137">OUTPUTS</span></span>

### <span data-ttu-id="6ba30-138">PSController 中的 DevSpaces。</span><span class="sxs-lookup"><span data-stu-id="6ba30-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="6ba30-139">筆記</span><span class="sxs-lookup"><span data-stu-id="6ba30-139">NOTES</span></span>

## <span data-ttu-id="6ba30-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ba30-140">RELATED LINKS</span></span>
