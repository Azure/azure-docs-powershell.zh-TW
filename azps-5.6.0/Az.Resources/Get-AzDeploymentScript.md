---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 7b61444bb4f3a23e1611e90b79545e1c174b0437
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903082"
---
# <span data-ttu-id="53f82-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="53f82-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="53f82-102">簡介</span><span class="sxs-lookup"><span data-stu-id="53f82-102">SYNOPSIS</span></span>
<span data-ttu-id="53f82-103">獲取或列出部署腳本。</span><span class="sxs-lookup"><span data-stu-id="53f82-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="53f82-104">語法</span><span class="sxs-lookup"><span data-stu-id="53f82-104">SYNTAX</span></span>

### <span data-ttu-id="53f82-105">ListDeploymentScript (預設) </span><span class="sxs-lookup"><span data-stu-id="53f82-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53f82-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="53f82-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53f82-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="53f82-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53f82-108">描述</span><span class="sxs-lookup"><span data-stu-id="53f82-108">DESCRIPTION</span></span>
<span data-ttu-id="53f82-109">**Get-AzDeploymentScript** Cmdlet 會取得單一部署腳本或部署腳本清單。</span><span class="sxs-lookup"><span data-stu-id="53f82-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="53f82-110">例子</span><span class="sxs-lookup"><span data-stu-id="53f82-110">EXAMPLES</span></span>

### <span data-ttu-id="53f82-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="53f82-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="53f82-112">以目前使用者的情況列出訂閱中的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="53f82-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="53f82-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="53f82-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="53f82-114">列出資源群組 DS-TestRg 中的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="53f82-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="53f82-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="53f82-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="53f82-116">在資源組 DS-TestRG 中，使用名稱為 MyDeploymentScript 的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="53f82-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="53f82-117">範例 4</span><span class="sxs-lookup"><span data-stu-id="53f82-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="53f82-118">使用具有給定資源識別碼的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="53f82-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="53f82-119">參數</span><span class="sxs-lookup"><span data-stu-id="53f82-119">PARAMETERS</span></span>

### <span data-ttu-id="53f82-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f82-120">-DefaultProfile</span></span>
<span data-ttu-id="53f82-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="53f82-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53f82-122">-Id</span><span class="sxs-lookup"><span data-stu-id="53f82-122">-Id</span></span>
<span data-ttu-id="53f82-123">部署腳本的完全合格的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="53f82-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="53f82-124">範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="53f82-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f82-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="53f82-125">-Name</span></span>
<span data-ttu-id="53f82-126">部署腳本的名稱</span><span class="sxs-lookup"><span data-stu-id="53f82-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f82-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f82-127">-ResourceGroupName</span></span>
<span data-ttu-id="53f82-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="53f82-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f82-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f82-129">CommonParameters</span></span>
<span data-ttu-id="53f82-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="53f82-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="53f82-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="53f82-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f82-132">輸入</span><span class="sxs-lookup"><span data-stu-id="53f82-132">INPUTS</span></span>

### <span data-ttu-id="53f82-133">System.String</span><span class="sxs-lookup"><span data-stu-id="53f82-133">System.String</span></span>

## <span data-ttu-id="53f82-134">輸出</span><span class="sxs-lookup"><span data-stu-id="53f82-134">OUTPUTS</span></span>

### <span data-ttu-id="53f82-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="53f82-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="53f82-136">筆記</span><span class="sxs-lookup"><span data-stu-id="53f82-136">NOTES</span></span>

## <span data-ttu-id="53f82-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="53f82-137">RELATED LINKS</span></span>