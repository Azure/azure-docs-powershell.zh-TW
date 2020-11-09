---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286303"
---
# <span data-ttu-id="29567-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="29567-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="29567-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29567-102">SYNOPSIS</span></span>
<span data-ttu-id="29567-103">在租使用者範圍中取得部署</span><span class="sxs-lookup"><span data-stu-id="29567-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="29567-104">句法</span><span class="sxs-lookup"><span data-stu-id="29567-104">SYNTAX</span></span>

### <span data-ttu-id="29567-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="29567-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29567-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="29567-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29567-107">說明</span><span class="sxs-lookup"><span data-stu-id="29567-107">DESCRIPTION</span></span>
<span data-ttu-id="29567-108">**AzTenantDeployment** Cmdlet 會取得租使用者範圍內的部署。</span><span class="sxs-lookup"><span data-stu-id="29567-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="29567-109">指定 *Name* 或 *Id* 參數來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="29567-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="29567-110">根據預設， **AzTenantDeployment 會取得** 租使用者範圍內的所有部署。</span><span class="sxs-lookup"><span data-stu-id="29567-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="29567-111">示例</span><span class="sxs-lookup"><span data-stu-id="29567-111">EXAMPLES</span></span>

### <span data-ttu-id="29567-112">範例1：取得租使用者範圍內的所有部署</span><span class="sxs-lookup"><span data-stu-id="29567-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="29567-113">這個命令會取得目前租使用者範圍內的所有部署。</span><span class="sxs-lookup"><span data-stu-id="29567-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="29567-114">範例2：依名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="29567-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="29567-115">這個命令會在目前的租使用者範圍內取得「Deploy01」部署。</span><span class="sxs-lookup"><span data-stu-id="29567-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="29567-116">您可以在使用 **新的 AzTenantDeployment** Cmdlet 建立部署時，將名稱指派給部署。</span><span class="sxs-lookup"><span data-stu-id="29567-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="29567-117">如果您沒有指派名稱，則 Cmdlet 會根據用來建立部署的範本，提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="29567-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="29567-118">範例3：依識別碼取得部署</span><span class="sxs-lookup"><span data-stu-id="29567-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="29567-119">這個命令會在租使用者範圍中取得「Deploy01」部署。</span><span class="sxs-lookup"><span data-stu-id="29567-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="29567-120">參數</span><span class="sxs-lookup"><span data-stu-id="29567-120">PARAMETERS</span></span>

### <span data-ttu-id="29567-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29567-121">-DefaultProfile</span></span>
<span data-ttu-id="29567-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29567-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29567-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="29567-123">-Id</span></span>
<span data-ttu-id="29567-124">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="29567-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="29567-125">範例：/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="29567-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29567-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="29567-126">-Name</span></span>
<span data-ttu-id="29567-127">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="29567-127">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29567-128">-預先</span><span class="sxs-lookup"><span data-stu-id="29567-128">-Pre</span></span>
<span data-ttu-id="29567-129">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="29567-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="29567-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29567-130">CommonParameters</span></span>
<span data-ttu-id="29567-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29567-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29567-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="29567-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29567-133">輸入</span><span class="sxs-lookup"><span data-stu-id="29567-133">INPUTS</span></span>

### <span data-ttu-id="29567-134">所有</span><span class="sxs-lookup"><span data-stu-id="29567-134">None</span></span>

## <span data-ttu-id="29567-135">輸出</span><span class="sxs-lookup"><span data-stu-id="29567-135">OUTPUTS</span></span>

### <span data-ttu-id="29567-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="29567-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="29567-137">筆記</span><span class="sxs-lookup"><span data-stu-id="29567-137">NOTES</span></span>

## <span data-ttu-id="29567-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="29567-138">RELATED LINKS</span></span>
