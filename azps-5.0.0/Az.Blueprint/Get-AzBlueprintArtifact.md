---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 725dca861c28f0194f800c80bd94d7e17efe15a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137557"
---
# <span data-ttu-id="34ac9-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="34ac9-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="34ac9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="34ac9-103">從藍圖定義中取得專案。</span><span class="sxs-lookup"><span data-stu-id="34ac9-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="34ac9-104">句法</span><span class="sxs-lookup"><span data-stu-id="34ac9-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34ac9-105">說明</span><span class="sxs-lookup"><span data-stu-id="34ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="34ac9-106">從藍圖定義中取得專案。</span><span class="sxs-lookup"><span data-stu-id="34ac9-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="34ac9-107">如果沒有指定藍圖定義版本，就會檢索草稿版本。</span><span class="sxs-lookup"><span data-stu-id="34ac9-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="34ac9-108">在沒有草稿版本的情況下，會傳回最新發佈的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="34ac9-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="34ac9-109">示例</span><span class="sxs-lookup"><span data-stu-id="34ac9-109">EXAMPLES</span></span>

### <span data-ttu-id="34ac9-110">範例1</span><span class="sxs-lookup"><span data-stu-id="34ac9-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192
```

<span data-ttu-id="34ac9-111">從藍圖定義中取得專案。</span><span class="sxs-lookup"><span data-stu-id="34ac9-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="34ac9-112">參數</span><span class="sxs-lookup"><span data-stu-id="34ac9-112">PARAMETERS</span></span>

### <span data-ttu-id="34ac9-113">-藍圖</span><span class="sxs-lookup"><span data-stu-id="34ac9-113">-Blueprint</span></span>
<span data-ttu-id="34ac9-114">藍圖物件。</span><span class="sxs-lookup"><span data-stu-id="34ac9-114">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34ac9-115">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="34ac9-115">-BlueprintVersion</span></span>
<span data-ttu-id="34ac9-116">取得工件的藍圖版本。</span><span class="sxs-lookup"><span data-stu-id="34ac9-116">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34ac9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ac9-117">-DefaultProfile</span></span>
<span data-ttu-id="34ac9-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34ac9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34ac9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="34ac9-119">-Name</span></span>
<span data-ttu-id="34ac9-120">專案名稱</span><span class="sxs-lookup"><span data-stu-id="34ac9-120">Name of the artifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ac9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ac9-121">CommonParameters</span></span>
<span data-ttu-id="34ac9-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34ac9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ac9-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="34ac9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ac9-124">輸入</span><span class="sxs-lookup"><span data-stu-id="34ac9-124">INPUTS</span></span>

### <span data-ttu-id="34ac9-125">System.object</span><span class="sxs-lookup"><span data-stu-id="34ac9-125">System.String</span></span>

### <span data-ttu-id="34ac9-126">PSArtifactKind 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="34ac9-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="34ac9-127">PSBlueprintBase 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="34ac9-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="34ac9-128">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="34ac9-128">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="34ac9-129">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="34ac9-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="34ac9-130">System.object []</span><span class="sxs-lookup"><span data-stu-id="34ac9-130">System.String[]</span></span>

## <span data-ttu-id="34ac9-131">輸出</span><span class="sxs-lookup"><span data-stu-id="34ac9-131">OUTPUTS</span></span>

### <span data-ttu-id="34ac9-132">PSBlueprintAssignment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="34ac9-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="34ac9-133">筆記</span><span class="sxs-lookup"><span data-stu-id="34ac9-133">NOTES</span></span>

## <span data-ttu-id="34ac9-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="34ac9-134">RELATED LINKS</span></span>
