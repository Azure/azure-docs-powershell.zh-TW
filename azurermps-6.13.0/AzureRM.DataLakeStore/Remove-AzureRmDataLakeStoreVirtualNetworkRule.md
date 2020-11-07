---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 196d0eba5119ab984f9ffc632a301d3e65157f63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624402"
---
# <span data-ttu-id="30794-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="30794-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="30794-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30794-102">SYNOPSIS</span></span>
<span data-ttu-id="30794-103">移除指定資料 Lake Store 中指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="30794-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30794-104">句法</span><span class="sxs-lookup"><span data-stu-id="30794-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30794-105">說明</span><span class="sxs-lookup"><span data-stu-id="30794-105">DESCRIPTION</span></span>
<span data-ttu-id="30794-106">**AzureRmDataLakeStoreVirtualNetworkRule** Cmdlet 會在指定的 Data Lake store 中移除指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="30794-106">The **Remove-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="30794-107">示例</span><span class="sxs-lookup"><span data-stu-id="30794-107">EXAMPLES</span></span>

### <span data-ttu-id="30794-108">範例1</span><span class="sxs-lookup"><span data-stu-id="30794-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="30794-109">從帳戶 "dls" 移除虛擬網路規則 "myVNET"</span><span class="sxs-lookup"><span data-stu-id="30794-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="30794-110">參數</span><span class="sxs-lookup"><span data-stu-id="30794-110">PARAMETERS</span></span>

### <span data-ttu-id="30794-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="30794-111">-Account</span></span>
<span data-ttu-id="30794-112">要在其中更新虛擬網路規則的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="30794-112">The Data Lake Store account to update the virtual network rule in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30794-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30794-113">-DefaultProfile</span></span>
<span data-ttu-id="30794-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30794-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30794-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="30794-115">-Name</span></span>
<span data-ttu-id="30794-116">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="30794-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30794-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30794-117">-PassThru</span></span>
<span data-ttu-id="30794-118">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="30794-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="30794-119">-確認</span><span class="sxs-lookup"><span data-stu-id="30794-119">-Confirm</span></span>
<span data-ttu-id="30794-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30794-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30794-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30794-121">-WhatIf</span></span>
<span data-ttu-id="30794-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30794-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30794-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30794-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30794-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30794-124">CommonParameters</span></span>
<span data-ttu-id="30794-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30794-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30794-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30794-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30794-127">輸入</span><span class="sxs-lookup"><span data-stu-id="30794-127">INPUTS</span></span>

### <span data-ttu-id="30794-128">System.object</span><span class="sxs-lookup"><span data-stu-id="30794-128">System.String</span></span>

### <span data-ttu-id="30794-129">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="30794-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="30794-130">輸出</span><span class="sxs-lookup"><span data-stu-id="30794-130">OUTPUTS</span></span>

### <span data-ttu-id="30794-131">System.object</span><span class="sxs-lookup"><span data-stu-id="30794-131">System.Boolean</span></span>

## <span data-ttu-id="30794-132">筆記</span><span class="sxs-lookup"><span data-stu-id="30794-132">NOTES</span></span>

## <span data-ttu-id="30794-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="30794-133">RELATED LINKS</span></span>
