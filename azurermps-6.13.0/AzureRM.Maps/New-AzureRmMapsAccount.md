---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccount.md
ms.openlocfilehash: 0b8bfad1b3bb9f24c6b7c74e92f64c64d776c2d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449757"
---
# <span data-ttu-id="8f259-101">New-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="8f259-101">New-AzureRmMapsAccount</span></span>

## <span data-ttu-id="8f259-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f259-102">SYNOPSIS</span></span>
<span data-ttu-id="8f259-103">建立 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="8f259-103">Creates an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f259-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f259-104">SYNTAX</span></span>

```
New-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f259-105">說明</span><span class="sxs-lookup"><span data-stu-id="8f259-105">DESCRIPTION</span></span>
<span data-ttu-id="8f259-106">New-AzureRmMapsAccount Cmdlet 會建立具有指定 SKU 的 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="8f259-106">The New-AzureRmMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="8f259-107">示例</span><span class="sxs-lookup"><span data-stu-id="8f259-107">EXAMPLES</span></span>

### <span data-ttu-id="8f259-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8f259-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="8f259-109">使用 SKU S0 和標記在資源群組 MyResourceGroup 中建立名為 [我的帳戶] 的新 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="8f259-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="8f259-110">參數</span><span class="sxs-lookup"><span data-stu-id="8f259-110">PARAMETERS</span></span>

### <span data-ttu-id="8f259-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f259-111">-DefaultProfile</span></span>
<span data-ttu-id="8f259-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f259-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f259-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8f259-113">-Force</span></span>
<span data-ttu-id="8f259-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="8f259-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8f259-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f259-115">-Name</span></span>
<span data-ttu-id="8f259-116">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8f259-116">Maps Account Name.</span></span>

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

### <span data-ttu-id="8f259-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f259-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f259-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8f259-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="8f259-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8f259-119">-SkuName</span></span>
<span data-ttu-id="8f259-120">地圖帳戶 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="8f259-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f259-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="8f259-121">-Tag</span></span>
<span data-ttu-id="8f259-122">地圖帳戶標籤。</span><span class="sxs-lookup"><span data-stu-id="8f259-122">Maps Account Tags.</span></span>

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

### <span data-ttu-id="8f259-123">-確認</span><span class="sxs-lookup"><span data-stu-id="8f259-123">-Confirm</span></span>
<span data-ttu-id="8f259-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8f259-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f259-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f259-125">-WhatIf</span></span>
<span data-ttu-id="8f259-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f259-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f259-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f259-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f259-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f259-128">CommonParameters</span></span>
<span data-ttu-id="8f259-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f259-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f259-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f259-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f259-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8f259-131">INPUTS</span></span>

### <span data-ttu-id="8f259-132">System.object</span><span class="sxs-lookup"><span data-stu-id="8f259-132">System.String</span></span>

## <span data-ttu-id="8f259-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8f259-133">OUTPUTS</span></span>

### <span data-ttu-id="8f259-134">PSMapsAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8f259-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="8f259-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8f259-135">NOTES</span></span>

## <span data-ttu-id="8f259-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f259-136">RELATED LINKS</span></span>
