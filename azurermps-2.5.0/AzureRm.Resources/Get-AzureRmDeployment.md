---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 1a86eb136fe976ba5e229ff36bd5d0e2a2cad340
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800305"
---
# <span data-ttu-id="4bb56-101">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="4bb56-101">Get-AzureRmDeployment</span></span>

## <span data-ttu-id="4bb56-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4bb56-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb56-103">取得部署</span><span class="sxs-lookup"><span data-stu-id="4bb56-103">Get deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bb56-104">句法</span><span class="sxs-lookup"><span data-stu-id="4bb56-104">SYNTAX</span></span>

### <span data-ttu-id="4bb56-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="4bb56-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bb56-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="4bb56-106">GetByDeploymentId</span></span>
```
Get-AzureRmDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bb56-107">說明</span><span class="sxs-lookup"><span data-stu-id="4bb56-107">DESCRIPTION</span></span>
<span data-ttu-id="4bb56-108">**AzureRmDeployment** Cmdlet 會取得目前訂閱範圍內的部署。</span><span class="sxs-lookup"><span data-stu-id="4bb56-108">The **Get-AzureRmDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="4bb56-109">指定 *Name* 或 *Id* 參數來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="4bb56-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="4bb56-110">根據預設， **AzureRmDeployment 會取得** 目前訂閱範圍中的所有部署。</span><span class="sxs-lookup"><span data-stu-id="4bb56-110">By default, **Get-AzureRmDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="4bb56-111">示例</span><span class="sxs-lookup"><span data-stu-id="4bb56-111">EXAMPLES</span></span>

### <span data-ttu-id="4bb56-112">範例1：取得訂閱範圍中的所有部署</span><span class="sxs-lookup"><span data-stu-id="4bb56-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzureRmDeployment
```

<span data-ttu-id="4bb56-113">這個命令會取得目前訂閱範圍中的所有部署。</span><span class="sxs-lookup"><span data-stu-id="4bb56-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="4bb56-114">範例2：依名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="4bb56-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "DeployRoles01"
```

<span data-ttu-id="4bb56-115">這個命令會在目前的訂閱範圍內取得 DeployRoles01 部署。</span><span class="sxs-lookup"><span data-stu-id="4bb56-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="4bb56-116">您可以在使用 **新的 AzureRmDeployment** Cmdlet 建立部署時，將名稱指派給部署。</span><span class="sxs-lookup"><span data-stu-id="4bb56-116">You can assign a name to a deployment when you create it by using the **New-AzureRmDeployment** cmdlets.</span></span>
<span data-ttu-id="4bb56-117">如果您沒有指派名稱，則 Cmdlet 會根據用來建立部署的範本，提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="4bb56-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="4bb56-118">參數</span><span class="sxs-lookup"><span data-stu-id="4bb56-118">PARAMETERS</span></span>

### <span data-ttu-id="4bb56-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4bb56-119">-ApiVersion</span></span>
<span data-ttu-id="4bb56-120">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4bb56-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4bb56-121">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="4bb56-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4bb56-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb56-122">-DefaultProfile</span></span>
<span data-ttu-id="4bb56-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bb56-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bb56-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="4bb56-124">-Id</span></span>
<span data-ttu-id="4bb56-125">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4bb56-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="4bb56-126">範例：/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="4bb56-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bb56-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="4bb56-127">-Name</span></span>
<span data-ttu-id="4bb56-128">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bb56-128">The name of deployment.</span></span>

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

### <span data-ttu-id="4bb56-129">-預先</span><span class="sxs-lookup"><span data-stu-id="4bb56-129">-Pre</span></span>
<span data-ttu-id="4bb56-130">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="4bb56-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4bb56-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb56-131">CommonParameters</span></span>
<span data-ttu-id="4bb56-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4bb56-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb56-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4bb56-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb56-134">輸入</span><span class="sxs-lookup"><span data-stu-id="4bb56-134">INPUTS</span></span>

### <span data-ttu-id="4bb56-135">System.object</span><span class="sxs-lookup"><span data-stu-id="4bb56-135">System.String</span></span>

## <span data-ttu-id="4bb56-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4bb56-136">OUTPUTS</span></span>

### <span data-ttu-id="4bb56-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="4bb56-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4bb56-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4bb56-138">NOTES</span></span>

## <span data-ttu-id="4bb56-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bb56-139">RELATED LINKS</span></span>
