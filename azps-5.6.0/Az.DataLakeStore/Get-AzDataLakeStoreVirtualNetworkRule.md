---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: ec5ac8ab949b95fba3f82ea795dadcecfac360ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908206"
---
# <span data-ttu-id="eba31-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="eba31-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="eba31-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eba31-102">SYNOPSIS</span></span>
<span data-ttu-id="eba31-103">在指定的 Data Lake Store 中，獲得指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="eba31-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="eba31-104">如果沒有指定虛擬網路規則，請列出帳戶的所有虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="eba31-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="eba31-105">語法</span><span class="sxs-lookup"><span data-stu-id="eba31-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eba31-106">描述</span><span class="sxs-lookup"><span data-stu-id="eba31-106">DESCRIPTION</span></span>
<span data-ttu-id="eba31-107">此Get-AzDataLakeStoreVirtualNetworkRule Cmdlet 會獲得指定 Data Lake Store 中指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="eba31-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="eba31-108">如果沒有指定虛擬網路規則，請列出帳戶的所有虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="eba31-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="eba31-109">例子</span><span class="sxs-lookup"><span data-stu-id="eba31-109">EXAMPLES</span></span>

### <span data-ttu-id="eba31-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="eba31-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="eba31-111">從帳戶 "dls" 中，將虛擬網路規則命名為 "myVNET"</span><span class="sxs-lookup"><span data-stu-id="eba31-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="eba31-112">參數</span><span class="sxs-lookup"><span data-stu-id="eba31-112">PARAMETERS</span></span>

### <span data-ttu-id="eba31-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="eba31-113">-Account</span></span>
<span data-ttu-id="eba31-114">資料湖市集帳戶，以從</span><span class="sxs-lookup"><span data-stu-id="eba31-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="eba31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba31-115">-DefaultProfile</span></span>
<span data-ttu-id="eba31-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eba31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eba31-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="eba31-117">-Name</span></span>
<span data-ttu-id="eba31-118">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="eba31-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="eba31-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba31-119">CommonParameters</span></span>
<span data-ttu-id="eba31-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eba31-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba31-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eba31-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba31-122">輸入</span><span class="sxs-lookup"><span data-stu-id="eba31-122">INPUTS</span></span>

### <span data-ttu-id="eba31-123">System.String</span><span class="sxs-lookup"><span data-stu-id="eba31-123">System.String</span></span>

## <span data-ttu-id="eba31-124">輸出</span><span class="sxs-lookup"><span data-stu-id="eba31-124">OUTPUTS</span></span>

### <span data-ttu-id="eba31-125">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="eba31-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="eba31-126">筆記</span><span class="sxs-lookup"><span data-stu-id="eba31-126">NOTES</span></span>

## <span data-ttu-id="eba31-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="eba31-127">RELATED LINKS</span></span>
