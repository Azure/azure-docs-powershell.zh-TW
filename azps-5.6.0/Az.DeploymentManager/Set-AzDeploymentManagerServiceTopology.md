---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7e3ed99abe5fb7a679506571d7d734cad02084d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905485"
---
# <span data-ttu-id="27794-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="27794-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="27794-102">簡介</span><span class="sxs-lookup"><span data-stu-id="27794-102">SYNOPSIS</span></span>
<span data-ttu-id="27794-103">更新服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="27794-103">Updates the service topology.</span></span>

## <span data-ttu-id="27794-104">語法</span><span class="sxs-lookup"><span data-stu-id="27794-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27794-105">描述</span><span class="sxs-lookup"><span data-stu-id="27794-105">DESCRIPTION</span></span>
<span data-ttu-id="27794-106">**Set-AzDeploymentManagerServiceTop用 Cmdlet** 會以指定的服務拓撲物件更新服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="27794-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="27794-107">Cmdlet 會返回更新的服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="27794-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="27794-108">例子</span><span class="sxs-lookup"><span data-stu-id="27794-108">EXAMPLES</span></span>

### <span data-ttu-id="27794-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="27794-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="27794-110">此命令會更新服務拓撲，其名稱和 ResourceGroup 會分別符合 $serviceTopologyObject 名稱及 ResourceGroupName 屬性。</span><span class="sxs-lookup"><span data-stu-id="27794-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="27794-111">該命令會返回更新的服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="27794-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="27794-112">參數</span><span class="sxs-lookup"><span data-stu-id="27794-112">PARAMETERS</span></span>

### <span data-ttu-id="27794-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27794-113">-DefaultProfile</span></span>
<span data-ttu-id="27794-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="27794-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27794-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27794-115">-InputObject</span></span>
<span data-ttu-id="27794-116">服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="27794-116">The service topology object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27794-117">-確認</span><span class="sxs-lookup"><span data-stu-id="27794-117">-Confirm</span></span>
<span data-ttu-id="27794-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="27794-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27794-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27794-119">-WhatIf</span></span>
<span data-ttu-id="27794-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27794-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27794-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27794-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27794-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27794-122">CommonParameters</span></span>
<span data-ttu-id="27794-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="27794-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27794-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27794-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27794-125">輸入</span><span class="sxs-lookup"><span data-stu-id="27794-125">INPUTS</span></span>

### <span data-ttu-id="27794-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopserviceserviceResource</span><span class="sxs-lookup"><span data-stu-id="27794-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="27794-127">輸出</span><span class="sxs-lookup"><span data-stu-id="27794-127">OUTPUTS</span></span>

### <span data-ttu-id="27794-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopserviceserviceResource</span><span class="sxs-lookup"><span data-stu-id="27794-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="27794-129">筆記</span><span class="sxs-lookup"><span data-stu-id="27794-129">NOTES</span></span>

## <span data-ttu-id="27794-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="27794-130">RELATED LINKS</span></span>
