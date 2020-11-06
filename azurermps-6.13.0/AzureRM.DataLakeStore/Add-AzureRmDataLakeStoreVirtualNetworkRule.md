---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: a25125b8aa76fa8d2be99f7f80b8fea2383bdf02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451227"
---
# <span data-ttu-id="80d61-101">Add-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="80d61-101">Add-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="80d61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80d61-102">SYNOPSIS</span></span>
<span data-ttu-id="80d61-103">將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="80d61-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80d61-104">句法</span><span class="sxs-lookup"><span data-stu-id="80d61-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80d61-105">說明</span><span class="sxs-lookup"><span data-stu-id="80d61-105">DESCRIPTION</span></span>
<span data-ttu-id="80d61-106">**AzureRmDataLakeStoreVirtualNetworkRule** Cmdlet 會將虛擬網路規則新增至指定的資料 Lake store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="80d61-106">The **Add-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="80d61-107">示例</span><span class="sxs-lookup"><span data-stu-id="80d61-107">EXAMPLES</span></span>

### <span data-ttu-id="80d61-108">範例1</span><span class="sxs-lookup"><span data-stu-id="80d61-108">Example 1</span></span>
```powershell
PS C:\> Add-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="80d61-109">這會建立名為 "myVNET" 的新虛擬網路規則，並以子網 id "testId" 的方式為 ""</span><span class="sxs-lookup"><span data-stu-id="80d61-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="80d61-110">參數</span><span class="sxs-lookup"><span data-stu-id="80d61-110">PARAMETERS</span></span>

### <span data-ttu-id="80d61-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="80d61-111">-Account</span></span>
<span data-ttu-id="80d61-112">要新增虛擬網路規則的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="80d61-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="80d61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d61-113">-DefaultProfile</span></span>
<span data-ttu-id="80d61-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80d61-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80d61-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="80d61-115">-Name</span></span>
<span data-ttu-id="80d61-116">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="80d61-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80d61-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="80d61-117">-SubnetId</span></span>
<span data-ttu-id="80d61-118">虛擬網路規則的 subnetId</span><span class="sxs-lookup"><span data-stu-id="80d61-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="80d61-119">-確認</span><span class="sxs-lookup"><span data-stu-id="80d61-119">-Confirm</span></span>
<span data-ttu-id="80d61-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80d61-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80d61-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80d61-121">-WhatIf</span></span>
<span data-ttu-id="80d61-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80d61-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80d61-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d61-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80d61-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d61-124">CommonParameters</span></span>
<span data-ttu-id="80d61-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80d61-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d61-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80d61-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d61-127">輸入</span><span class="sxs-lookup"><span data-stu-id="80d61-127">INPUTS</span></span>

### <span data-ttu-id="80d61-128">System.object</span><span class="sxs-lookup"><span data-stu-id="80d61-128">System.String</span></span>

## <span data-ttu-id="80d61-129">輸出</span><span class="sxs-lookup"><span data-stu-id="80d61-129">OUTPUTS</span></span>

### <span data-ttu-id="80d61-130">DataLakeStoreVirtualNetworkRule 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="80d61-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="80d61-131">筆記</span><span class="sxs-lookup"><span data-stu-id="80d61-131">NOTES</span></span>

## <span data-ttu-id="80d61-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="80d61-132">RELATED LINKS</span></span>
