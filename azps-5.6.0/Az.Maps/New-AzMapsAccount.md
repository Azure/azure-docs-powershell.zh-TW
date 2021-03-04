---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: b6a2e27f18a0ae9b7c98239d5acd1073922e149e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916121"
---
# <span data-ttu-id="c87cc-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c87cc-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="c87cc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c87cc-102">SYNOPSIS</span></span>
<span data-ttu-id="c87cc-103">建立 Azure 地圖服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="c87cc-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="c87cc-104">語法</span><span class="sxs-lookup"><span data-stu-id="c87cc-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c87cc-105">描述</span><span class="sxs-lookup"><span data-stu-id="c87cc-105">DESCRIPTION</span></span>
<span data-ttu-id="c87cc-106">Cmdlet New-AzMapsAccount會使用指定的 SKU 建立 Azure 地圖服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="c87cc-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="c87cc-107">例子</span><span class="sxs-lookup"><span data-stu-id="c87cc-107">EXAMPLES</span></span>

### <span data-ttu-id="c87cc-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c87cc-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="c87cc-109">在資源群組 MyResourceGroup 中，使用 SKU S0 和標記，建立名為 MyAccount 的新 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="c87cc-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="c87cc-110">參數</span><span class="sxs-lookup"><span data-stu-id="c87cc-110">PARAMETERS</span></span>

### <span data-ttu-id="c87cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c87cc-111">-DefaultProfile</span></span>
<span data-ttu-id="c87cc-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c87cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c87cc-113">-強制</span><span class="sxs-lookup"><span data-stu-id="c87cc-113">-Force</span></span>
<span data-ttu-id="c87cc-114">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="c87cc-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c87cc-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c87cc-115">-Name</span></span>
<span data-ttu-id="c87cc-116">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c87cc-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c87cc-117">-ResourceGroupName</span></span>
<span data-ttu-id="c87cc-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c87cc-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87cc-119">-SKUName</span><span class="sxs-lookup"><span data-stu-id="c87cc-119">-SkuName</span></span>
<span data-ttu-id="c87cc-120">地圖帳戶 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="c87cc-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87cc-121">-標記</span><span class="sxs-lookup"><span data-stu-id="c87cc-121">-Tag</span></span>
<span data-ttu-id="c87cc-122">地圖帳戶標記。</span><span class="sxs-lookup"><span data-stu-id="c87cc-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c87cc-123">-確認</span><span class="sxs-lookup"><span data-stu-id="c87cc-123">-Confirm</span></span>
<span data-ttu-id="c87cc-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c87cc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c87cc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c87cc-125">-WhatIf</span></span>
<span data-ttu-id="c87cc-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c87cc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c87cc-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c87cc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c87cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87cc-128">CommonParameters</span></span>
<span data-ttu-id="c87cc-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c87cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87cc-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c87cc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87cc-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c87cc-131">INPUTS</span></span>

### <span data-ttu-id="c87cc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c87cc-132">System.String</span></span>

## <span data-ttu-id="c87cc-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c87cc-133">OUTPUTS</span></span>

### <span data-ttu-id="c87cc-134">Microsoft.Azure.Commands.Maps.models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c87cc-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="c87cc-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c87cc-135">NOTES</span></span>

## <span data-ttu-id="c87cc-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c87cc-136">RELATED LINKS</span></span>
