---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435519"
---
# <span data-ttu-id="cf210-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="cf210-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="cf210-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf210-102">SYNOPSIS</span></span>
<span data-ttu-id="cf210-103">取得管理群組部署的部署作業</span><span class="sxs-lookup"><span data-stu-id="cf210-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="cf210-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf210-104">SYNTAX</span></span>

### <span data-ttu-id="cf210-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="cf210-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf210-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="cf210-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf210-107">說明</span><span class="sxs-lookup"><span data-stu-id="cf210-107">DESCRIPTION</span></span>
<span data-ttu-id="cf210-108">**AzManagementGroupDeploymentOperation** Cmdlet 會列出屬於管理群組部署的所有作業，以協助您識別並提供有關特定部署失敗之確切作業的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="cf210-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="cf210-109">這與入口網站上的部署詳細資料中提供的資訊相同。</span><span class="sxs-lookup"><span data-stu-id="cf210-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="cf210-110">示例</span><span class="sxs-lookup"><span data-stu-id="cf210-110">EXAMPLES</span></span>

### <span data-ttu-id="cf210-111">範例1：取得給定部署名稱的部署作業</span><span class="sxs-lookup"><span data-stu-id="cf210-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="cf210-112">取得管理群組 "myMG" 中名稱為 "Deploy01" 的部署作業。</span><span class="sxs-lookup"><span data-stu-id="cf210-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="cf210-113">範例2：取得部署並取得其部署作業</span><span class="sxs-lookup"><span data-stu-id="cf210-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="cf210-114">這個命令會在管理群組 "myMG" 中取得部署 "Deploy01"，並取得其部署作業。</span><span class="sxs-lookup"><span data-stu-id="cf210-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="cf210-115">參數</span><span class="sxs-lookup"><span data-stu-id="cf210-115">PARAMETERS</span></span>

### <span data-ttu-id="cf210-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf210-116">-DefaultProfile</span></span>
<span data-ttu-id="cf210-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf210-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf210-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="cf210-118">-DeploymentName</span></span>
<span data-ttu-id="cf210-119">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="cf210-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf210-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="cf210-120">-DeploymentObject</span></span>
<span data-ttu-id="cf210-121">部署物件。</span><span class="sxs-lookup"><span data-stu-id="cf210-121">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf210-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="cf210-122">-ManagementGroupId</span></span>
<span data-ttu-id="cf210-123">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf210-123">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf210-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="cf210-124">-OperationId</span></span>
<span data-ttu-id="cf210-125">部署操作 Id。</span><span class="sxs-lookup"><span data-stu-id="cf210-125">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf210-126">-預先</span><span class="sxs-lookup"><span data-stu-id="cf210-126">-Pre</span></span>
<span data-ttu-id="cf210-127">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="cf210-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="cf210-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf210-128">CommonParameters</span></span>
<span data-ttu-id="cf210-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf210-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf210-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cf210-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf210-131">輸入</span><span class="sxs-lookup"><span data-stu-id="cf210-131">INPUTS</span></span>

### <span data-ttu-id="cf210-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="cf210-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="cf210-133">輸出</span><span class="sxs-lookup"><span data-stu-id="cf210-133">OUTPUTS</span></span>

### <span data-ttu-id="cf210-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="cf210-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="cf210-135">筆記</span><span class="sxs-lookup"><span data-stu-id="cf210-135">NOTES</span></span>

## <span data-ttu-id="cf210-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf210-136">RELATED LINKS</span></span>
