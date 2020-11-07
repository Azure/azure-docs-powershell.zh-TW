---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
ms.openlocfilehash: fa7ea6f1e53b94a349d51856432f1c01b2e89ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624577"
---
# <span data-ttu-id="8f3b3-101">New-AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="8f3b3-101">New-AzureRmSearchAdminKey</span></span>

## <span data-ttu-id="8f3b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f3b3-102">SYNOPSIS</span></span>
<span data-ttu-id="8f3b3-103">再生 Azure 搜尋服務的管理員金鑰。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-103">Regenerates an admin key of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f3b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f3b3-104">SYNTAX</span></span>

### <span data-ttu-id="8f3b3-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8f3b3-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f3b3-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f3b3-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f3b3-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f3b3-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f3b3-108">說明</span><span class="sxs-lookup"><span data-stu-id="8f3b3-108">DESCRIPTION</span></span>
<span data-ttu-id="8f3b3-109">**新的-AzureRmSearchAdminKey** Cmdlet 會重新產生 Azure 搜尋服務的管理員金鑰。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-109">The **New-AzureRmSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="8f3b3-110">示例</span><span class="sxs-lookup"><span data-stu-id="8f3b3-110">EXAMPLES</span></span>

### <span data-ttu-id="8f3b3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8f3b3-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="8f3b3-112">此範例會再生 Azure 搜尋服務的主鍵。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="8f3b3-113">參數</span><span class="sxs-lookup"><span data-stu-id="8f3b3-113">PARAMETERS</span></span>

### <span data-ttu-id="8f3b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f3b3-114">-DefaultProfile</span></span>
<span data-ttu-id="8f3b3-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8f3b3-116">-Force</span></span>
<span data-ttu-id="8f3b3-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8f3b3-118">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="8f3b3-118">-KeyKind</span></span>
<span data-ttu-id="8f3b3-119">搜尋服務管理員金鑰類型 (主要/次要) 。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-119">Search Service admin key kind (Primary/Secondary).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKeyKind
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b3-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8f3b3-120">-ParentObject</span></span>
<span data-ttu-id="8f3b3-121">搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-121">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b3-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8f3b3-122">-ParentResourceId</span></span>
<span data-ttu-id="8f3b3-123">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-123">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f3b3-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f3b3-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b3-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8f3b3-126">-ServiceName</span></span>
<span data-ttu-id="8f3b3-127">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-127">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b3-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8f3b3-128">-Confirm</span></span>
<span data-ttu-id="8f3b3-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f3b3-130">-WhatIf</span></span>
<span data-ttu-id="8f3b3-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f3b3-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3b3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f3b3-133">CommonParameters</span></span>
<span data-ttu-id="8f3b3-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f3b3-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f3b3-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8f3b3-136">INPUTS</span></span>

### <span data-ttu-id="8f3b3-137">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="8f3b3-138">參數： ParentObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="8f3b3-138">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="8f3b3-139">System.object</span><span class="sxs-lookup"><span data-stu-id="8f3b3-139">System.String</span></span>

## <span data-ttu-id="8f3b3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8f3b3-140">OUTPUTS</span></span>

### <span data-ttu-id="8f3b3-141">[PSSearchAdminKey]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="8f3b3-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="8f3b3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8f3b3-142">NOTES</span></span>

## <span data-ttu-id="8f3b3-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f3b3-143">RELATED LINKS</span></span>

[<span data-ttu-id="8f3b3-144">AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="8f3b3-144">Get-AzureRmSearchAdminKeyPair</span></span>](./Get-AzureRmSearchAdminKeyPair.md)
