---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284786"
---
# <span data-ttu-id="a90bb-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="a90bb-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="a90bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a90bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a90bb-103">更新服務。</span><span class="sxs-lookup"><span data-stu-id="a90bb-103">Updates the service.</span></span>

## <span data-ttu-id="a90bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="a90bb-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a90bb-105">說明</span><span class="sxs-lookup"><span data-stu-id="a90bb-105">DESCRIPTION</span></span>
<span data-ttu-id="a90bb-106">**AzDeploymentManagerService** Cmdlet 會使用指定的服務物件更新服務。</span><span class="sxs-lookup"><span data-stu-id="a90bb-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="a90bb-107">這個 Cmdlet 會傳回更新的服務物件。</span><span class="sxs-lookup"><span data-stu-id="a90bb-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="a90bb-108">示例</span><span class="sxs-lookup"><span data-stu-id="a90bb-108">EXAMPLES</span></span>

### <span data-ttu-id="a90bb-109">範例1</span><span class="sxs-lookup"><span data-stu-id="a90bb-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="a90bb-110">這個命令會分別更新 name、service 拓朴名稱和 ResourceGroup 的服務，分別與 $serviceObject 的 Name、ServiceTopologyName 和 ResourceGroupName 屬性相符。</span><span class="sxs-lookup"><span data-stu-id="a90bb-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="a90bb-111">該服務將會更新為 $serviceObject 中設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="a90bb-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="a90bb-112">參數</span><span class="sxs-lookup"><span data-stu-id="a90bb-112">PARAMETERS</span></span>

### <span data-ttu-id="a90bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a90bb-113">-DefaultProfile</span></span>
<span data-ttu-id="a90bb-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a90bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a90bb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a90bb-115">-InputObject</span></span>
<span data-ttu-id="a90bb-116">服務物件。</span><span class="sxs-lookup"><span data-stu-id="a90bb-116">The service object.</span></span>

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

### <span data-ttu-id="a90bb-117">-確認</span><span class="sxs-lookup"><span data-stu-id="a90bb-117">-Confirm</span></span>
<span data-ttu-id="a90bb-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a90bb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a90bb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a90bb-119">-WhatIf</span></span>
<span data-ttu-id="a90bb-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a90bb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a90bb-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a90bb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a90bb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a90bb-122">CommonParameters</span></span>
<span data-ttu-id="a90bb-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a90bb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a90bb-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a90bb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a90bb-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a90bb-125">INPUTS</span></span>

### <span data-ttu-id="a90bb-126">PSServiceResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="a90bb-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="a90bb-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a90bb-127">OUTPUTS</span></span>

### <span data-ttu-id="a90bb-128">PSServiceResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="a90bb-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="a90bb-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a90bb-129">NOTES</span></span>

## <span data-ttu-id="a90bb-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a90bb-130">RELATED LINKS</span></span>
