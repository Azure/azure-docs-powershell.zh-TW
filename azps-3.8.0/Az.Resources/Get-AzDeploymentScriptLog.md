---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 855127362fbcbf906755affde0bec6de5e7f2698
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965765"
---
# <span data-ttu-id="f40de-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f40de-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="f40de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f40de-102">SYNOPSIS</span></span>
<span data-ttu-id="f40de-103">取得部署腳本執行的記錄。</span><span class="sxs-lookup"><span data-stu-id="f40de-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="f40de-104">句法</span><span class="sxs-lookup"><span data-stu-id="f40de-104">SYNTAX</span></span>

### <span data-ttu-id="f40de-105">GetDeploymentScriptLogByName (預設) </span><span class="sxs-lookup"><span data-stu-id="f40de-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f40de-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="f40de-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f40de-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="f40de-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f40de-108">說明</span><span class="sxs-lookup"><span data-stu-id="f40de-108">DESCRIPTION</span></span>
<span data-ttu-id="f40de-109">**AzDeploymentScriptLog** Cmdlet 會取得部署腳本執行的記錄。</span><span class="sxs-lookup"><span data-stu-id="f40de-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="f40de-110">示例</span><span class="sxs-lookup"><span data-stu-id="f40de-110">EXAMPLES</span></span>

### <span data-ttu-id="f40de-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f40de-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="f40de-112">取得資源群組 DS-TestRG 中名稱為 MyDeploymentScript 的部署腳本記錄。</span><span class="sxs-lookup"><span data-stu-id="f40de-112">Gets log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="f40de-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f40de-113">Example 2</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="f40de-114">第一個命令會在資源群組 DS-TestRG 中取得名稱為 MyDeploymentScript 的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="f40de-114">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="f40de-115">第二個命令會取得給定部署腳本的記錄。</span><span class="sxs-lookup"><span data-stu-id="f40de-115">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="f40de-116">參數</span><span class="sxs-lookup"><span data-stu-id="f40de-116">PARAMETERS</span></span>

### <span data-ttu-id="f40de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f40de-117">-DefaultProfile</span></span>
<span data-ttu-id="f40de-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f40de-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f40de-119">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="f40de-119">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="f40de-120">[部署腳本 PowerShell] 物件。</span><span class="sxs-lookup"><span data-stu-id="f40de-120">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f40de-121">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="f40de-121">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="f40de-122">部署腳本的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f40de-122">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="f40de-123">範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="f40de-123">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40de-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f40de-124">-Name</span></span>
<span data-ttu-id="f40de-125">部署腳本的名稱。</span><span class="sxs-lookup"><span data-stu-id="f40de-125">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f40de-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f40de-126">-ResourceGroupName</span></span>
<span data-ttu-id="f40de-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f40de-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f40de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f40de-128">CommonParameters</span></span>
<span data-ttu-id="f40de-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f40de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f40de-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f40de-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f40de-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f40de-131">INPUTS</span></span>

### <span data-ttu-id="f40de-132">System.object</span><span class="sxs-lookup"><span data-stu-id="f40de-132">System.String</span></span>

### <span data-ttu-id="f40de-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="f40de-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="f40de-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f40de-134">OUTPUTS</span></span>

### <span data-ttu-id="f40de-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f40de-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="f40de-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f40de-136">NOTES</span></span>

## <span data-ttu-id="f40de-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f40de-137">RELATED LINKS</span></span>
