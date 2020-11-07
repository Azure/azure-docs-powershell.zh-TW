---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: c3218141e495bb92216e254830ddaa7dd7a0a0c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959720"
---
# <span data-ttu-id="201ae-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="201ae-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="201ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="201ae-102">SYNOPSIS</span></span>
<span data-ttu-id="201ae-103">在租使用者範圍中取得部署</span><span class="sxs-lookup"><span data-stu-id="201ae-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="201ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="201ae-104">SYNTAX</span></span>

### <span data-ttu-id="201ae-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="201ae-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201ae-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="201ae-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="201ae-107">說明</span><span class="sxs-lookup"><span data-stu-id="201ae-107">DESCRIPTION</span></span>
<span data-ttu-id="201ae-108">**AzTenantDeployment** Cmdlet 會取得租使用者範圍內的部署。</span><span class="sxs-lookup"><span data-stu-id="201ae-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="201ae-109">指定 *Name* 或 *Id* 參數來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="201ae-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="201ae-110">根據預設， **AzTenantDeployment 會取得** 租使用者範圍內的所有部署。</span><span class="sxs-lookup"><span data-stu-id="201ae-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="201ae-111">示例</span><span class="sxs-lookup"><span data-stu-id="201ae-111">EXAMPLES</span></span>

### <span data-ttu-id="201ae-112">範例1：取得租使用者範圍內的所有部署</span><span class="sxs-lookup"><span data-stu-id="201ae-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="201ae-113">這個命令會取得目前租使用者範圍內的所有部署。</span><span class="sxs-lookup"><span data-stu-id="201ae-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="201ae-114">範例2：依名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="201ae-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="201ae-115">這個命令會在目前的租使用者範圍內取得「Deploy01」部署。</span><span class="sxs-lookup"><span data-stu-id="201ae-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="201ae-116">您可以在使用 **新的 AzTenantDeployment** Cmdlet 建立部署時，將名稱指派給部署。</span><span class="sxs-lookup"><span data-stu-id="201ae-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="201ae-117">如果您沒有指派名稱，則 Cmdlet 會根據用來建立部署的範本，提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="201ae-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="201ae-118">範例3：依識別碼取得部署</span><span class="sxs-lookup"><span data-stu-id="201ae-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="201ae-119">這個命令會在租使用者範圍中取得「Deploy01」部署。</span><span class="sxs-lookup"><span data-stu-id="201ae-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="201ae-120">參數</span><span class="sxs-lookup"><span data-stu-id="201ae-120">PARAMETERS</span></span>

### <span data-ttu-id="201ae-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="201ae-121">-ApiVersion</span></span>
<span data-ttu-id="201ae-122">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="201ae-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="201ae-123">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="201ae-123">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201ae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201ae-124">-DefaultProfile</span></span>
<span data-ttu-id="201ae-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="201ae-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201ae-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="201ae-126">-Id</span></span>
<span data-ttu-id="201ae-127">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="201ae-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="201ae-128">範例：/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="201ae-128">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201ae-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="201ae-129">-Name</span></span>
<span data-ttu-id="201ae-130">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="201ae-130">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201ae-131">-預先</span><span class="sxs-lookup"><span data-stu-id="201ae-131">-Pre</span></span>
<span data-ttu-id="201ae-132">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="201ae-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201ae-133">CommonParameters</span></span>
<span data-ttu-id="201ae-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="201ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201ae-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="201ae-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201ae-136">輸入</span><span class="sxs-lookup"><span data-stu-id="201ae-136">INPUTS</span></span>

### <span data-ttu-id="201ae-137">所有</span><span class="sxs-lookup"><span data-stu-id="201ae-137">None</span></span>

## <span data-ttu-id="201ae-138">輸出</span><span class="sxs-lookup"><span data-stu-id="201ae-138">OUTPUTS</span></span>

### <span data-ttu-id="201ae-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="201ae-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="201ae-140">筆記</span><span class="sxs-lookup"><span data-stu-id="201ae-140">NOTES</span></span>

## <span data-ttu-id="201ae-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="201ae-141">RELATED LINKS</span></span>
