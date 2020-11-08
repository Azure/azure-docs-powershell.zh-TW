---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 9e455b7160b731f20e5dad6230b2015f73ca5390
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969291"
---
# <span data-ttu-id="a4ef6-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a4ef6-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="a4ef6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4ef6-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ef6-103">移除指定資料 Lake Store 中指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a4ef6-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a4ef6-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4ef6-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4ef6-105">說明</span><span class="sxs-lookup"><span data-stu-id="a4ef6-105">DESCRIPTION</span></span>
<span data-ttu-id="a4ef6-106">**AzDataLakeStoreVirtualNetworkRule** Cmdlet 會在指定的 Data Lake store 中移除指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a4ef6-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a4ef6-107">示例</span><span class="sxs-lookup"><span data-stu-id="a4ef6-107">EXAMPLES</span></span>

### <span data-ttu-id="a4ef6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a4ef6-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="a4ef6-109">從帳戶 "dls" 移除虛擬網路規則 "myVNET"</span><span class="sxs-lookup"><span data-stu-id="a4ef6-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="a4ef6-110">參數</span><span class="sxs-lookup"><span data-stu-id="a4ef6-110">PARAMETERS</span></span>

### <span data-ttu-id="a4ef6-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a4ef6-111">-Account</span></span>
<span data-ttu-id="a4ef6-112">要在其中更新虛擬網路規則的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="a4ef6-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="a4ef6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ef6-113">-DefaultProfile</span></span>
<span data-ttu-id="a4ef6-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4ef6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ef6-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4ef6-115">-Name</span></span>
<span data-ttu-id="a4ef6-116">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4ef6-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="a4ef6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4ef6-117">-PassThru</span></span>
<span data-ttu-id="a4ef6-118">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="a4ef6-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="a4ef6-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a4ef6-119">-Confirm</span></span>
<span data-ttu-id="a4ef6-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4ef6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4ef6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4ef6-121">-WhatIf</span></span>
<span data-ttu-id="a4ef6-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4ef6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4ef6-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4ef6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4ef6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ef6-124">CommonParameters</span></span>
<span data-ttu-id="a4ef6-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4ef6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ef6-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a4ef6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ef6-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a4ef6-127">INPUTS</span></span>

### <span data-ttu-id="a4ef6-128">System.object</span><span class="sxs-lookup"><span data-stu-id="a4ef6-128">System.String</span></span>

## <span data-ttu-id="a4ef6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a4ef6-129">OUTPUTS</span></span>

### <span data-ttu-id="a4ef6-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a4ef6-130">System.Boolean</span></span>

## <span data-ttu-id="a4ef6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a4ef6-131">NOTES</span></span>

## <span data-ttu-id="a4ef6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4ef6-132">RELATED LINKS</span></span>