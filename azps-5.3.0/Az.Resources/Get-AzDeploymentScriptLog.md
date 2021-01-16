---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435533"
---
# <span data-ttu-id="56c0b-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="56c0b-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="56c0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="56c0b-103">取得部署腳本執行的記錄。</span><span class="sxs-lookup"><span data-stu-id="56c0b-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="56c0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="56c0b-104">SYNTAX</span></span>

### <span data-ttu-id="56c0b-105">GetDeploymentScriptLogByName (預設) </span><span class="sxs-lookup"><span data-stu-id="56c0b-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56c0b-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="56c0b-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56c0b-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="56c0b-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56c0b-108">說明</span><span class="sxs-lookup"><span data-stu-id="56c0b-108">DESCRIPTION</span></span>
<span data-ttu-id="56c0b-109">**AzDeploymentScriptLog** Cmdlet 會取得部署腳本執行的記錄。</span><span class="sxs-lookup"><span data-stu-id="56c0b-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="56c0b-110">示例</span><span class="sxs-lookup"><span data-stu-id="56c0b-110">EXAMPLES</span></span>

### <span data-ttu-id="56c0b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="56c0b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="56c0b-112">取得資源群組 DS-TestRG 中名稱為 MyDeploymentScript 的部署腳本記錄。</span><span class="sxs-lookup"><span data-stu-id="56c0b-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="56c0b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="56c0b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="56c0b-114">取得資源群組 DS-TestRG 中名稱為 MyDeploymentScript 之部署腳本記錄的最後3行。</span><span class="sxs-lookup"><span data-stu-id="56c0b-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="56c0b-115">範例3</span><span class="sxs-lookup"><span data-stu-id="56c0b-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="56c0b-116">第一個命令會在資源群組 DS-TestRG 中取得名稱為 MyDeploymentScript 的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="56c0b-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="56c0b-117">第二個命令會取得給定部署腳本的記錄。</span><span class="sxs-lookup"><span data-stu-id="56c0b-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="56c0b-118">參數</span><span class="sxs-lookup"><span data-stu-id="56c0b-118">PARAMETERS</span></span>

### <span data-ttu-id="56c0b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c0b-119">-DefaultProfile</span></span>
<span data-ttu-id="56c0b-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56c0b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56c0b-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="56c0b-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="56c0b-122">[部署腳本 PowerShell] 物件。</span><span class="sxs-lookup"><span data-stu-id="56c0b-122">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56c0b-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="56c0b-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="56c0b-124">部署腳本的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="56c0b-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="56c0b-125">範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="56c0b-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56c0b-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="56c0b-126">-Name</span></span>
<span data-ttu-id="56c0b-127">部署腳本的名稱。</span><span class="sxs-lookup"><span data-stu-id="56c0b-127">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c0b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56c0b-128">-ResourceGroupName</span></span>
<span data-ttu-id="56c0b-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="56c0b-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c0b-130">-尾</span><span class="sxs-lookup"><span data-stu-id="56c0b-130">-Tail</span></span>
<span data-ttu-id="56c0b-131">將輸出限制為最後 n 行</span><span class="sxs-lookup"><span data-stu-id="56c0b-131">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56c0b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c0b-132">CommonParameters</span></span>
<span data-ttu-id="56c0b-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56c0b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c0b-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="56c0b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c0b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="56c0b-135">INPUTS</span></span>

### <span data-ttu-id="56c0b-136">System.object</span><span class="sxs-lookup"><span data-stu-id="56c0b-136">System.String</span></span>

### <span data-ttu-id="56c0b-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="56c0b-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="56c0b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="56c0b-138">OUTPUTS</span></span>

### <span data-ttu-id="56c0b-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="56c0b-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="56c0b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="56c0b-140">NOTES</span></span>

## <span data-ttu-id="56c0b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="56c0b-141">RELATED LINKS</span></span>
