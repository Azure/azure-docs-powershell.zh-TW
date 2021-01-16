---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 75ebbe0eedd9aad396500701d5e94efff76069f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273896"
---
# <span data-ttu-id="b0a19-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="b0a19-101">Get-AzDeployment</span></span>

## <span data-ttu-id="b0a19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0a19-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a19-103">取得部署</span><span class="sxs-lookup"><span data-stu-id="b0a19-103">Get deployment</span></span>

## <span data-ttu-id="b0a19-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0a19-104">SYNTAX</span></span>

### <span data-ttu-id="b0a19-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="b0a19-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0a19-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b0a19-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0a19-107">說明</span><span class="sxs-lookup"><span data-stu-id="b0a19-107">DESCRIPTION</span></span>
<span data-ttu-id="b0a19-108">**AzDeployment** Cmdlet 會取得目前訂閱範圍內的部署。</span><span class="sxs-lookup"><span data-stu-id="b0a19-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="b0a19-109">指定 *Name* 或 *Id* 參數來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="b0a19-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="b0a19-110">根據預設， **AzDeployment 會取得** 目前訂閱範圍中的所有部署。</span><span class="sxs-lookup"><span data-stu-id="b0a19-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="b0a19-111">示例</span><span class="sxs-lookup"><span data-stu-id="b0a19-111">EXAMPLES</span></span>

### <span data-ttu-id="b0a19-112">範例1：取得訂閱範圍中的所有部署</span><span class="sxs-lookup"><span data-stu-id="b0a19-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="b0a19-113">這個命令會取得目前訂閱範圍中的所有部署。</span><span class="sxs-lookup"><span data-stu-id="b0a19-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="b0a19-114">範例2：依名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="b0a19-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="b0a19-115">這個命令會在目前的訂閱範圍內取得 DeployRoles01 部署。</span><span class="sxs-lookup"><span data-stu-id="b0a19-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="b0a19-116">您可以在使用 **新的 AzDeployment** Cmdlet 建立部署時，將名稱指派給部署。</span><span class="sxs-lookup"><span data-stu-id="b0a19-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="b0a19-117">如果您沒有指派名稱，則 Cmdlet 會根據用來建立部署的範本，提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="b0a19-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="b0a19-118">參數</span><span class="sxs-lookup"><span data-stu-id="b0a19-118">PARAMETERS</span></span>

### <span data-ttu-id="b0a19-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a19-119">-DefaultProfile</span></span>
<span data-ttu-id="b0a19-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0a19-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0a19-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b0a19-121">-Id</span></span>
<span data-ttu-id="b0a19-122">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0a19-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="b0a19-123">範例：/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="b0a19-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="b0a19-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0a19-124">-Name</span></span>
<span data-ttu-id="b0a19-125">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0a19-125">The name of deployment.</span></span>

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

### <span data-ttu-id="b0a19-126">-預先</span><span class="sxs-lookup"><span data-stu-id="b0a19-126">-Pre</span></span>
<span data-ttu-id="b0a19-127">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="b0a19-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b0a19-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a19-128">CommonParameters</span></span>
<span data-ttu-id="b0a19-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0a19-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a19-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b0a19-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a19-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b0a19-131">INPUTS</span></span>

### <span data-ttu-id="b0a19-132">所有</span><span class="sxs-lookup"><span data-stu-id="b0a19-132">None</span></span>

## <span data-ttu-id="b0a19-133">輸出</span><span class="sxs-lookup"><span data-stu-id="b0a19-133">OUTPUTS</span></span>

### <span data-ttu-id="b0a19-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="b0a19-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b0a19-135">筆記</span><span class="sxs-lookup"><span data-stu-id="b0a19-135">NOTES</span></span>

## <span data-ttu-id="b0a19-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0a19-136">RELATED LINKS</span></span>
