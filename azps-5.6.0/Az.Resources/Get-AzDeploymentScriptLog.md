---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: dc62e4766a83e1a2046b15fbdf6619e08c4b8e28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903081"
---
# <span data-ttu-id="f0379-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f0379-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="f0379-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f0379-102">SYNOPSIS</span></span>
<span data-ttu-id="f0379-103">獲得部署腳本執行的記錄。</span><span class="sxs-lookup"><span data-stu-id="f0379-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="f0379-104">語法</span><span class="sxs-lookup"><span data-stu-id="f0379-104">SYNTAX</span></span>

### <span data-ttu-id="f0379-105">GetDeploymentScriptLogByName (預設) </span><span class="sxs-lookup"><span data-stu-id="f0379-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0379-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="f0379-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0379-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="f0379-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0379-108">描述</span><span class="sxs-lookup"><span data-stu-id="f0379-108">DESCRIPTION</span></span>
<span data-ttu-id="f0379-109">**Get-AzDeploymentScriptLog** Cmdlet 會取得部署腳本執行的記錄。</span><span class="sxs-lookup"><span data-stu-id="f0379-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="f0379-110">例子</span><span class="sxs-lookup"><span data-stu-id="f0379-110">EXAMPLES</span></span>

### <span data-ttu-id="f0379-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f0379-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="f0379-112">在資源組 DS-TestRG 中，以名稱 MyDeploymentScript 來記錄部署腳本。</span><span class="sxs-lookup"><span data-stu-id="f0379-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="f0379-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="f0379-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="f0379-114">在資源組 DS-TestRG 中，使用名稱為 MyDeploymentScript 的部署腳本記錄的最後 3 行。</span><span class="sxs-lookup"><span data-stu-id="f0379-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="f0379-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="f0379-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="f0379-116">第一個命令會獲得資源群組 DS-TestRG 中名稱為 MyDeploymentScript 的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="f0379-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="f0379-117">第二個命令會獲得給定部署腳本的記錄。</span><span class="sxs-lookup"><span data-stu-id="f0379-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="f0379-118">參數</span><span class="sxs-lookup"><span data-stu-id="f0379-118">PARAMETERS</span></span>

### <span data-ttu-id="f0379-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0379-119">-DefaultProfile</span></span>
<span data-ttu-id="f0379-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0379-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0379-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="f0379-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="f0379-122">部署腳本 PowerShell 物件。</span><span class="sxs-lookup"><span data-stu-id="f0379-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="f0379-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="f0379-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="f0379-124">部署腳本的完全合格的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0379-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="f0379-125">範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="f0379-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="f0379-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0379-126">-Name</span></span>
<span data-ttu-id="f0379-127">部署腳本的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0379-127">The name of the deployment script.</span></span>

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

### <span data-ttu-id="f0379-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0379-128">-ResourceGroupName</span></span>
<span data-ttu-id="f0379-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0379-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="f0379-130">-Tail</span><span class="sxs-lookup"><span data-stu-id="f0379-130">-Tail</span></span>
<span data-ttu-id="f0379-131">將輸出限制為最後 n 行</span><span class="sxs-lookup"><span data-stu-id="f0379-131">Limit output to last n lines</span></span>

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

### <span data-ttu-id="f0379-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0379-132">CommonParameters</span></span>
<span data-ttu-id="f0379-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f0379-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0379-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0379-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0379-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f0379-135">INPUTS</span></span>

### <span data-ttu-id="f0379-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f0379-136">System.String</span></span>

### <span data-ttu-id="f0379-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="f0379-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="f0379-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f0379-138">OUTPUTS</span></span>

### <span data-ttu-id="f0379-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f0379-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="f0379-140">筆記</span><span class="sxs-lookup"><span data-stu-id="f0379-140">NOTES</span></span>

## <span data-ttu-id="f0379-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0379-141">RELATED LINKS</span></span>
