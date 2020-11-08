---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 75ebbe0eedd9aad396500701d5e94efff76069f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137355"
---
# <span data-ttu-id="9e183-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="9e183-101">Get-AzDeployment</span></span>

## <span data-ttu-id="9e183-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e183-102">SYNOPSIS</span></span>
<span data-ttu-id="9e183-103">取得部署</span><span class="sxs-lookup"><span data-stu-id="9e183-103">Get deployment</span></span>

## <span data-ttu-id="9e183-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e183-104">SYNTAX</span></span>

### <span data-ttu-id="9e183-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="9e183-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e183-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="9e183-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e183-107">說明</span><span class="sxs-lookup"><span data-stu-id="9e183-107">DESCRIPTION</span></span>
<span data-ttu-id="9e183-108">**AzDeployment** Cmdlet 會取得目前訂閱範圍內的部署。</span><span class="sxs-lookup"><span data-stu-id="9e183-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="9e183-109">指定 *Name* 或 *Id* 參數來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="9e183-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="9e183-110">根據預設， **AzDeployment 會取得** 目前訂閱範圍中的所有部署。</span><span class="sxs-lookup"><span data-stu-id="9e183-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="9e183-111">示例</span><span class="sxs-lookup"><span data-stu-id="9e183-111">EXAMPLES</span></span>

### <span data-ttu-id="9e183-112">範例1：取得訂閱範圍中的所有部署</span><span class="sxs-lookup"><span data-stu-id="9e183-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="9e183-113">這個命令會取得目前訂閱範圍中的所有部署。</span><span class="sxs-lookup"><span data-stu-id="9e183-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="9e183-114">範例2：依名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="9e183-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="9e183-115">這個命令會在目前的訂閱範圍內取得 DeployRoles01 部署。</span><span class="sxs-lookup"><span data-stu-id="9e183-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="9e183-116">您可以在使用 **新的 AzDeployment** Cmdlet 建立部署時，將名稱指派給部署。</span><span class="sxs-lookup"><span data-stu-id="9e183-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="9e183-117">如果您沒有指派名稱，則 Cmdlet 會根據用來建立部署的範本，提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="9e183-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="9e183-118">參數</span><span class="sxs-lookup"><span data-stu-id="9e183-118">PARAMETERS</span></span>

### <span data-ttu-id="9e183-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e183-119">-DefaultProfile</span></span>
<span data-ttu-id="9e183-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e183-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e183-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="9e183-121">-Id</span></span>
<span data-ttu-id="9e183-122">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e183-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="9e183-123">範例：/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="9e183-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="9e183-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e183-124">-Name</span></span>
<span data-ttu-id="9e183-125">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e183-125">The name of deployment.</span></span>

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

### <span data-ttu-id="9e183-126">-預先</span><span class="sxs-lookup"><span data-stu-id="9e183-126">-Pre</span></span>
<span data-ttu-id="9e183-127">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="9e183-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9e183-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e183-128">CommonParameters</span></span>
<span data-ttu-id="9e183-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e183-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e183-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9e183-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e183-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9e183-131">INPUTS</span></span>

### <span data-ttu-id="9e183-132">所有</span><span class="sxs-lookup"><span data-stu-id="9e183-132">None</span></span>

## <span data-ttu-id="9e183-133">輸出</span><span class="sxs-lookup"><span data-stu-id="9e183-133">OUTPUTS</span></span>

### <span data-ttu-id="9e183-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="9e183-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9e183-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9e183-135">NOTES</span></span>

## <span data-ttu-id="9e183-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e183-136">RELATED LINKS</span></span>
