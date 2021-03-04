---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: b5b9f154cb494aad7c1ef0faec130b4c4c1cc3d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904501"
---
# <span data-ttu-id="6a805-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6a805-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="6a805-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6a805-102">SYNOPSIS</span></span>
<span data-ttu-id="6a805-103">移除指定 Data Lake Store 中指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="6a805-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="6a805-104">語法</span><span class="sxs-lookup"><span data-stu-id="6a805-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a805-105">描述</span><span class="sxs-lookup"><span data-stu-id="6a805-105">DESCRIPTION</span></span>
<span data-ttu-id="6a805-106">**Remove-AzDataLakeStoreVirtualNetworkRule** Cmdlet 會移除指定 Data Lake Store 中指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="6a805-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="6a805-107">例子</span><span class="sxs-lookup"><span data-stu-id="6a805-107">EXAMPLES</span></span>

### <span data-ttu-id="6a805-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6a805-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="6a805-109">從帳戶 "dls" 移除虛擬網路規則 "myVNET"</span><span class="sxs-lookup"><span data-stu-id="6a805-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="6a805-110">參數</span><span class="sxs-lookup"><span data-stu-id="6a805-110">PARAMETERS</span></span>

### <span data-ttu-id="6a805-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="6a805-111">-Account</span></span>
<span data-ttu-id="6a805-112">Data Lake 市集帳戶以更新</span><span class="sxs-lookup"><span data-stu-id="6a805-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="6a805-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a805-113">-DefaultProfile</span></span>
<span data-ttu-id="6a805-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a805-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a805-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a805-115">-Name</span></span>
<span data-ttu-id="6a805-116">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a805-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="6a805-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a805-117">-PassThru</span></span>
<span data-ttu-id="6a805-118">表示應該會返回布林值回應，指出刪除作業的結果。</span><span class="sxs-lookup"><span data-stu-id="6a805-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="6a805-119">-確認</span><span class="sxs-lookup"><span data-stu-id="6a805-119">-Confirm</span></span>
<span data-ttu-id="6a805-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6a805-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a805-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a805-121">-WhatIf</span></span>
<span data-ttu-id="6a805-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6a805-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a805-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6a805-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a805-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a805-124">CommonParameters</span></span>
<span data-ttu-id="6a805-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6a805-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a805-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6a805-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a805-127">輸入</span><span class="sxs-lookup"><span data-stu-id="6a805-127">INPUTS</span></span>

### <span data-ttu-id="6a805-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6a805-128">System.String</span></span>

## <span data-ttu-id="6a805-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6a805-129">OUTPUTS</span></span>

### <span data-ttu-id="6a805-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a805-130">System.Boolean</span></span>

## <span data-ttu-id="6a805-131">筆記</span><span class="sxs-lookup"><span data-stu-id="6a805-131">NOTES</span></span>

## <span data-ttu-id="6a805-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a805-132">RELATED LINKS</span></span>
