---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: f8412ac037372d89373c64c77f43c10db1730100
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905478"
---
# <span data-ttu-id="ece3d-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="ece3d-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="ece3d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ece3d-102">SYNOPSIS</span></span>
<span data-ttu-id="ece3d-103">更新步驟。</span><span class="sxs-lookup"><span data-stu-id="ece3d-103">Updates the step.</span></span>

## <span data-ttu-id="ece3d-104">語法</span><span class="sxs-lookup"><span data-stu-id="ece3d-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece3d-105">描述</span><span class="sxs-lookup"><span data-stu-id="ece3d-105">DESCRIPTION</span></span>
<span data-ttu-id="ece3d-106">**Set-AzDeploymentManagerStep** Cmdlet 會以指定的步驟物件更新步驟。</span><span class="sxs-lookup"><span data-stu-id="ece3d-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="ece3d-107">Cmdlet 會返回更新的步驟物件。</span><span class="sxs-lookup"><span data-stu-id="ece3d-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="ece3d-108">例子</span><span class="sxs-lookup"><span data-stu-id="ece3d-108">EXAMPLES</span></span>

### <span data-ttu-id="ece3d-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="ece3d-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="ece3d-110">此命令會更新一個步驟，其名稱和 ResourceGroup 會分別符合 $stepObject 名稱及 ResourceGroupName 屬性。</span><span class="sxs-lookup"><span data-stu-id="ece3d-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="ece3d-111">步驟會更新為 $stepObject。</span><span class="sxs-lookup"><span data-stu-id="ece3d-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="ece3d-112">參數</span><span class="sxs-lookup"><span data-stu-id="ece3d-112">PARAMETERS</span></span>

### <span data-ttu-id="ece3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece3d-113">-DefaultProfile</span></span>
<span data-ttu-id="ece3d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ece3d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ece3d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ece3d-115">-InputObject</span></span>
<span data-ttu-id="ece3d-116">步驟物件。</span><span class="sxs-lookup"><span data-stu-id="ece3d-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ece3d-117">-確認</span><span class="sxs-lookup"><span data-stu-id="ece3d-117">-Confirm</span></span>
<span data-ttu-id="ece3d-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ece3d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece3d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece3d-119">-WhatIf</span></span>
<span data-ttu-id="ece3d-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ece3d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ece3d-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ece3d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece3d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece3d-122">CommonParameters</span></span>
<span data-ttu-id="ece3d-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ece3d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece3d-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ece3d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece3d-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ece3d-125">INPUTS</span></span>

### <span data-ttu-id="ece3d-126">Microsoft.Azure.Commands.DeploymentManager.models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="ece3d-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="ece3d-127">輸出</span><span class="sxs-lookup"><span data-stu-id="ece3d-127">OUTPUTS</span></span>

### <span data-ttu-id="ece3d-128">Microsoft.Azure.Commands.DeploymentManager.models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="ece3d-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="ece3d-129">筆記</span><span class="sxs-lookup"><span data-stu-id="ece3d-129">NOTES</span></span>

## <span data-ttu-id="ece3d-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ece3d-130">RELATED LINKS</span></span>
