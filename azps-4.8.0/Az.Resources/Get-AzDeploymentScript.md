---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 761969eea685c21bc513efdfde9ea79a9e1e4a70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126926"
---
# <span data-ttu-id="761d7-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="761d7-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="761d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="761d7-102">SYNOPSIS</span></span>
<span data-ttu-id="761d7-103">取得或列出部署腳本。</span><span class="sxs-lookup"><span data-stu-id="761d7-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="761d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="761d7-104">SYNTAX</span></span>

### <span data-ttu-id="761d7-105">ListDeploymentScript (預設) </span><span class="sxs-lookup"><span data-stu-id="761d7-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="761d7-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="761d7-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="761d7-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="761d7-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="761d7-108">說明</span><span class="sxs-lookup"><span data-stu-id="761d7-108">DESCRIPTION</span></span>
<span data-ttu-id="761d7-109">**AzDeploymentScript** Cmdlet 會取得單一部署腳本或部署腳本清單。</span><span class="sxs-lookup"><span data-stu-id="761d7-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="761d7-110">示例</span><span class="sxs-lookup"><span data-stu-id="761d7-110">EXAMPLES</span></span>

### <span data-ttu-id="761d7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="761d7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="761d7-112">在目前使用者的內容中，列出訂閱中的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="761d7-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="761d7-113">範例2</span><span class="sxs-lookup"><span data-stu-id="761d7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="761d7-114">列出資源群組 DS 中的部署腳本-TestRg。</span><span class="sxs-lookup"><span data-stu-id="761d7-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="761d7-115">範例3</span><span class="sxs-lookup"><span data-stu-id="761d7-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="761d7-116">取得資源群組 DS-TestRG 中名稱為 MyDeploymentScript 的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="761d7-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="761d7-117">範例4</span><span class="sxs-lookup"><span data-stu-id="761d7-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="761d7-118">取得具有指定資源識別碼的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="761d7-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="761d7-119">參數</span><span class="sxs-lookup"><span data-stu-id="761d7-119">PARAMETERS</span></span>

### <span data-ttu-id="761d7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="761d7-120">-DefaultProfile</span></span>
<span data-ttu-id="761d7-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="761d7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="761d7-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="761d7-122">-Id</span></span>
<span data-ttu-id="761d7-123">部署腳本的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="761d7-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="761d7-124">範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="761d7-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="761d7-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="761d7-125">-Name</span></span>
<span data-ttu-id="761d7-126">部署腳本的名稱</span><span class="sxs-lookup"><span data-stu-id="761d7-126">The name of the deployment script</span></span>

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

### <span data-ttu-id="761d7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="761d7-127">-ResourceGroupName</span></span>
<span data-ttu-id="761d7-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="761d7-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="761d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="761d7-129">CommonParameters</span></span>
<span data-ttu-id="761d7-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="761d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="761d7-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="761d7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="761d7-132">輸入</span><span class="sxs-lookup"><span data-stu-id="761d7-132">INPUTS</span></span>

### <span data-ttu-id="761d7-133">System.object</span><span class="sxs-lookup"><span data-stu-id="761d7-133">System.String</span></span>

## <span data-ttu-id="761d7-134">輸出</span><span class="sxs-lookup"><span data-stu-id="761d7-134">OUTPUTS</span></span>

### <span data-ttu-id="761d7-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="761d7-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="761d7-136">筆記</span><span class="sxs-lookup"><span data-stu-id="761d7-136">NOTES</span></span>

## <span data-ttu-id="761d7-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="761d7-137">RELATED LINKS</span></span>
