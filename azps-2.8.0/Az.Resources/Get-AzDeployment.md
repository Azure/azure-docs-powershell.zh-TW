---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: cde9c4f8827840047e7fa4a1c597ed6338ed8e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791294"
---
# <span data-ttu-id="c2ec5-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="c2ec5-101">Get-AzDeployment</span></span>

## <span data-ttu-id="c2ec5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ec5-103">取得部署</span><span class="sxs-lookup"><span data-stu-id="c2ec5-103">Get deployment</span></span>

## <span data-ttu-id="c2ec5-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2ec5-104">SYNTAX</span></span>

### <span data-ttu-id="c2ec5-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="c2ec5-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2ec5-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c2ec5-106">GetByDeploymentId</span></span>
```
Get-AzDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2ec5-107">說明</span><span class="sxs-lookup"><span data-stu-id="c2ec5-107">DESCRIPTION</span></span>
<span data-ttu-id="c2ec5-108">**AzDeployment** Cmdlet 會取得目前訂閱範圍內的部署。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="c2ec5-109">指定 *Name* 或 *Id* 參數來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="c2ec5-110">根據預設， **AzDeployment 會取得** 目前訂閱範圍中的所有部署。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="c2ec5-111">示例</span><span class="sxs-lookup"><span data-stu-id="c2ec5-111">EXAMPLES</span></span>

### <span data-ttu-id="c2ec5-112">範例1：取得訂閱範圍中的所有部署</span><span class="sxs-lookup"><span data-stu-id="c2ec5-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="c2ec5-113">這個命令會取得目前訂閱範圍中的所有部署。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="c2ec5-114">範例2：依名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="c2ec5-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="c2ec5-115">這個命令會在目前的訂閱範圍內取得 DeployRoles01 部署。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="c2ec5-116">您可以在使用 **新的 AzDeployment** Cmdlet 建立部署時，將名稱指派給部署。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="c2ec5-117">如果您沒有指派名稱，則 Cmdlet 會根據用來建立部署的範本，提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="c2ec5-118">參數</span><span class="sxs-lookup"><span data-stu-id="c2ec5-118">PARAMETERS</span></span>

### <span data-ttu-id="c2ec5-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c2ec5-119">-ApiVersion</span></span>
<span data-ttu-id="c2ec5-120">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c2ec5-121">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c2ec5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ec5-122">-DefaultProfile</span></span>
<span data-ttu-id="c2ec5-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2ec5-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="c2ec5-124">-Id</span></span>
<span data-ttu-id="c2ec5-125">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c2ec5-126">範例：/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c2ec5-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ec5-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2ec5-127">-Name</span></span>
<span data-ttu-id="c2ec5-128">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-128">The name of deployment.</span></span>

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

### <span data-ttu-id="c2ec5-129">-預先</span><span class="sxs-lookup"><span data-stu-id="c2ec5-129">-Pre</span></span>
<span data-ttu-id="c2ec5-130">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c2ec5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ec5-131">CommonParameters</span></span>
<span data-ttu-id="c2ec5-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ec5-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2ec5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ec5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c2ec5-134">INPUTS</span></span>

### <span data-ttu-id="c2ec5-135">所有</span><span class="sxs-lookup"><span data-stu-id="c2ec5-135">None</span></span>

## <span data-ttu-id="c2ec5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c2ec5-136">OUTPUTS</span></span>

### <span data-ttu-id="c2ec5-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c2ec5-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c2ec5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c2ec5-138">NOTES</span></span>

## <span data-ttu-id="c2ec5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2ec5-139">RELATED LINKS</span></span>
