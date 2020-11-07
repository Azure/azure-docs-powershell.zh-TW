---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 4820a1aec02355a535ec7798eb7f8e3dba6458b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798433"
---
# <span data-ttu-id="4e7b2-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="4e7b2-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="4e7b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="4e7b2-103">取得管理群組部署的部署作業</span><span class="sxs-lookup"><span data-stu-id="4e7b2-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="4e7b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e7b2-104">SYNTAX</span></span>

### <span data-ttu-id="4e7b2-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="4e7b2-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e7b2-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4e7b2-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e7b2-107">說明</span><span class="sxs-lookup"><span data-stu-id="4e7b2-107">DESCRIPTION</span></span>
<span data-ttu-id="4e7b2-108">**AzManagementGroupDeploymentOperation** Cmdlet 會列出屬於管理群組部署的所有作業，以協助您識別並提供有關特定部署失敗之確切作業的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="4e7b2-109">這與入口網站上的部署詳細資料中提供的資訊相同。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="4e7b2-110">示例</span><span class="sxs-lookup"><span data-stu-id="4e7b2-110">EXAMPLES</span></span>

### <span data-ttu-id="4e7b2-111">範例1：取得給定部署名稱的部署作業</span><span class="sxs-lookup"><span data-stu-id="4e7b2-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="4e7b2-112">取得管理群組 "myMG" 中名稱為 "Deploy01" 的部署作業。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="4e7b2-113">範例2：取得部署並取得其部署作業</span><span class="sxs-lookup"><span data-stu-id="4e7b2-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="4e7b2-114">這個命令會在管理群組 "myMG" 中取得部署 "Deploy01"，並取得其部署作業。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="4e7b2-115">參數</span><span class="sxs-lookup"><span data-stu-id="4e7b2-115">PARAMETERS</span></span>

### <span data-ttu-id="4e7b2-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4e7b2-116">-ApiVersion</span></span>
<span data-ttu-id="4e7b2-117">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4e7b2-118">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4e7b2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e7b2-119">-DefaultProfile</span></span>
<span data-ttu-id="4e7b2-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e7b2-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="4e7b2-121">-DeploymentName</span></span>
<span data-ttu-id="4e7b2-122">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-122">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e7b2-123">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4e7b2-123">-DeploymentObject</span></span>
<span data-ttu-id="4e7b2-124">部署物件。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-124">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e7b2-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="4e7b2-125">-ManagementGroupId</span></span>
<span data-ttu-id="4e7b2-126">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-126">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e7b2-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="4e7b2-127">-OperationId</span></span>
<span data-ttu-id="4e7b2-128">部署操作 Id。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-128">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e7b2-129">-預先</span><span class="sxs-lookup"><span data-stu-id="4e7b2-129">-Pre</span></span>
<span data-ttu-id="4e7b2-130">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4e7b2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e7b2-131">CommonParameters</span></span>
<span data-ttu-id="4e7b2-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e7b2-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e7b2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e7b2-134">輸入</span><span class="sxs-lookup"><span data-stu-id="4e7b2-134">INPUTS</span></span>

### <span data-ttu-id="4e7b2-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="4e7b2-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4e7b2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4e7b2-136">OUTPUTS</span></span>

### <span data-ttu-id="4e7b2-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="4e7b2-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="4e7b2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4e7b2-138">NOTES</span></span>

## <span data-ttu-id="4e7b2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e7b2-139">RELATED LINKS</span></span>
