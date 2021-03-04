---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: 4c33ba2bd87e1f6103454740529c5570ef04ea17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905489"
---
# <span data-ttu-id="c1098-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="c1098-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="c1098-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1098-102">SYNOPSIS</span></span>
<span data-ttu-id="c1098-103">更新服務。</span><span class="sxs-lookup"><span data-stu-id="c1098-103">Updates the service.</span></span>

## <span data-ttu-id="c1098-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1098-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1098-105">描述</span><span class="sxs-lookup"><span data-stu-id="c1098-105">DESCRIPTION</span></span>
<span data-ttu-id="c1098-106">**Set-AzDeploymentManagerService** Cmdlet 會以指定的服務物件更新服務。</span><span class="sxs-lookup"><span data-stu-id="c1098-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="c1098-107">Cmdlet 會返回更新的服務物件。</span><span class="sxs-lookup"><span data-stu-id="c1098-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="c1098-108">例子</span><span class="sxs-lookup"><span data-stu-id="c1098-108">EXAMPLES</span></span>

### <span data-ttu-id="c1098-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="c1098-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="c1098-110">此命令會更新服務，其名稱、服務拓撲名稱及 ResourceGroup 會分別符合名稱、ServiceTop用Name 和 ResourceGroupName 屬性$serviceObject名稱。</span><span class="sxs-lookup"><span data-stu-id="c1098-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="c1098-111">服務會更新為 $serviceObject。</span><span class="sxs-lookup"><span data-stu-id="c1098-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="c1098-112">參數</span><span class="sxs-lookup"><span data-stu-id="c1098-112">PARAMETERS</span></span>

### <span data-ttu-id="c1098-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1098-113">-DefaultProfile</span></span>
<span data-ttu-id="c1098-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1098-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1098-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1098-115">-InputObject</span></span>
<span data-ttu-id="c1098-116">服務物件。</span><span class="sxs-lookup"><span data-stu-id="c1098-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1098-117">-確認</span><span class="sxs-lookup"><span data-stu-id="c1098-117">-Confirm</span></span>
<span data-ttu-id="c1098-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c1098-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1098-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1098-119">-WhatIf</span></span>
<span data-ttu-id="c1098-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1098-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1098-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1098-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1098-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1098-122">CommonParameters</span></span>
<span data-ttu-id="c1098-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1098-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1098-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1098-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1098-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c1098-125">INPUTS</span></span>

### <span data-ttu-id="c1098-126">Microsoft.Azure.Commands.DeploymentManager.models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="c1098-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="c1098-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c1098-127">OUTPUTS</span></span>

### <span data-ttu-id="c1098-128">Microsoft.Azure.Commands.DeploymentManager.models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="c1098-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="c1098-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c1098-129">NOTES</span></span>

## <span data-ttu-id="c1098-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1098-130">RELATED LINKS</span></span>
