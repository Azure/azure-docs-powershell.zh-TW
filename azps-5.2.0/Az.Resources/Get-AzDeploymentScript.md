---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: b5c3ca86129e622a90a84d099961a8f8dd433eef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273883"
---
# <span data-ttu-id="ac490-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="ac490-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="ac490-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac490-102">SYNOPSIS</span></span>
<span data-ttu-id="ac490-103">取得或列出部署腳本。</span><span class="sxs-lookup"><span data-stu-id="ac490-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="ac490-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac490-104">SYNTAX</span></span>

### <span data-ttu-id="ac490-105">ListDeploymentScript (預設) </span><span class="sxs-lookup"><span data-stu-id="ac490-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac490-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="ac490-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac490-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac490-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac490-108">說明</span><span class="sxs-lookup"><span data-stu-id="ac490-108">DESCRIPTION</span></span>
<span data-ttu-id="ac490-109">**AzDeploymentScript** Cmdlet 會取得單一部署腳本或部署腳本清單。</span><span class="sxs-lookup"><span data-stu-id="ac490-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="ac490-110">示例</span><span class="sxs-lookup"><span data-stu-id="ac490-110">EXAMPLES</span></span>

### <span data-ttu-id="ac490-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ac490-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="ac490-112">在目前使用者的內容中，列出訂閱中的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="ac490-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="ac490-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ac490-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="ac490-114">列出資源群組 DS 中的部署腳本-TestRg。</span><span class="sxs-lookup"><span data-stu-id="ac490-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="ac490-115">範例3</span><span class="sxs-lookup"><span data-stu-id="ac490-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="ac490-116">取得資源群組 DS-TestRG 中名稱為 MyDeploymentScript 的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="ac490-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="ac490-117">範例4</span><span class="sxs-lookup"><span data-stu-id="ac490-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="ac490-118">取得具有指定資源識別碼的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="ac490-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="ac490-119">參數</span><span class="sxs-lookup"><span data-stu-id="ac490-119">PARAMETERS</span></span>

### <span data-ttu-id="ac490-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac490-120">-DefaultProfile</span></span>
<span data-ttu-id="ac490-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac490-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac490-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ac490-122">-Id</span></span>
<span data-ttu-id="ac490-123">部署腳本的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac490-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="ac490-124">範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="ac490-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="ac490-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac490-125">-Name</span></span>
<span data-ttu-id="ac490-126">部署腳本的名稱</span><span class="sxs-lookup"><span data-stu-id="ac490-126">The name of the deployment script</span></span>

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

### <span data-ttu-id="ac490-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac490-127">-ResourceGroupName</span></span>
<span data-ttu-id="ac490-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac490-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="ac490-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac490-129">CommonParameters</span></span>
<span data-ttu-id="ac490-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac490-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ac490-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac490-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac490-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ac490-132">INPUTS</span></span>

### <span data-ttu-id="ac490-133">System.object</span><span class="sxs-lookup"><span data-stu-id="ac490-133">System.String</span></span>

## <span data-ttu-id="ac490-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ac490-134">OUTPUTS</span></span>

### <span data-ttu-id="ac490-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="ac490-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="ac490-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ac490-136">NOTES</span></span>

## <span data-ttu-id="ac490-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac490-137">RELATED LINKS</span></span>