---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 1e6358972e547e6a5fab54072396c3ad6fc7f418
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141550"
---
# <span data-ttu-id="77f55-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="77f55-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="77f55-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77f55-102">SYNOPSIS</span></span>
<span data-ttu-id="77f55-103">建立 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="77f55-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="77f55-104">句法</span><span class="sxs-lookup"><span data-stu-id="77f55-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77f55-105">說明</span><span class="sxs-lookup"><span data-stu-id="77f55-105">DESCRIPTION</span></span>
<span data-ttu-id="77f55-106">New-AzMapsAccount Cmdlet 會建立具有指定 SKU 的 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="77f55-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="77f55-107">示例</span><span class="sxs-lookup"><span data-stu-id="77f55-107">EXAMPLES</span></span>

### <span data-ttu-id="77f55-108">範例1</span><span class="sxs-lookup"><span data-stu-id="77f55-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="77f55-109">使用 SKU S0 和標記在資源群組 MyResourceGroup 中建立名為 [我的帳戶] 的新 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="77f55-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="77f55-110">參數</span><span class="sxs-lookup"><span data-stu-id="77f55-110">PARAMETERS</span></span>

### <span data-ttu-id="77f55-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f55-111">-DefaultProfile</span></span>
<span data-ttu-id="77f55-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77f55-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77f55-113">-Force</span><span class="sxs-lookup"><span data-stu-id="77f55-113">-Force</span></span>
<span data-ttu-id="77f55-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="77f55-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="77f55-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="77f55-115">-Name</span></span>
<span data-ttu-id="77f55-116">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="77f55-116">Maps Account Name.</span></span>

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

### <span data-ttu-id="77f55-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f55-117">-ResourceGroupName</span></span>
<span data-ttu-id="77f55-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="77f55-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="77f55-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="77f55-119">-SkuName</span></span>
<span data-ttu-id="77f55-120">地圖帳戶 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="77f55-120">Maps Account Sku Name.</span></span>

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

### <span data-ttu-id="77f55-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="77f55-121">-Tag</span></span>
<span data-ttu-id="77f55-122">地圖帳戶標籤。</span><span class="sxs-lookup"><span data-stu-id="77f55-122">Maps Account Tags.</span></span>

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

### <span data-ttu-id="77f55-123">-確認</span><span class="sxs-lookup"><span data-stu-id="77f55-123">-Confirm</span></span>
<span data-ttu-id="77f55-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="77f55-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77f55-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77f55-125">-WhatIf</span></span>
<span data-ttu-id="77f55-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="77f55-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77f55-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77f55-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77f55-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f55-128">CommonParameters</span></span>
<span data-ttu-id="77f55-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77f55-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f55-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77f55-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f55-131">輸入</span><span class="sxs-lookup"><span data-stu-id="77f55-131">INPUTS</span></span>

### <span data-ttu-id="77f55-132">System.object</span><span class="sxs-lookup"><span data-stu-id="77f55-132">System.String</span></span>

## <span data-ttu-id="77f55-133">輸出</span><span class="sxs-lookup"><span data-stu-id="77f55-133">OUTPUTS</span></span>

### <span data-ttu-id="77f55-134">PSMapsAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="77f55-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="77f55-135">筆記</span><span class="sxs-lookup"><span data-stu-id="77f55-135">NOTES</span></span>

## <span data-ttu-id="77f55-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="77f55-136">RELATED LINKS</span></span>