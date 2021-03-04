---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: e5b6c552d736571acb484ca301372e9eb32d3944
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916158"
---
# <span data-ttu-id="69588-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="69588-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="69588-102">簡介</span><span class="sxs-lookup"><span data-stu-id="69588-102">SYNOPSIS</span></span>
<span data-ttu-id="69588-103">新增虛擬網路規則至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="69588-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="69588-104">語法</span><span class="sxs-lookup"><span data-stu-id="69588-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69588-105">描述</span><span class="sxs-lookup"><span data-stu-id="69588-105">DESCRIPTION</span></span>
<span data-ttu-id="69588-106">**Add-AzDataLakeStoreVirtualNetworkRule** Cmdlet 會新增虛擬網路規則至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="69588-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="69588-107">例子</span><span class="sxs-lookup"><span data-stu-id="69588-107">EXAMPLES</span></span>

### <span data-ttu-id="69588-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="69588-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="69588-109">這會在帳戶 "dls" 中使用子網識別碼 "testId" 建立名為 "myVNET" 的新虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="69588-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="69588-110">參數</span><span class="sxs-lookup"><span data-stu-id="69588-110">PARAMETERS</span></span>

### <span data-ttu-id="69588-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="69588-111">-Account</span></span>
<span data-ttu-id="69588-112">資料湖市集帳戶以新增虛擬網路規則至</span><span class="sxs-lookup"><span data-stu-id="69588-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="69588-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69588-113">-DefaultProfile</span></span>
<span data-ttu-id="69588-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="69588-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69588-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="69588-115">-Name</span></span>
<span data-ttu-id="69588-116">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="69588-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="69588-117">-子網Id</span><span class="sxs-lookup"><span data-stu-id="69588-117">-SubnetId</span></span>
<span data-ttu-id="69588-118">虛擬網路規則的子網Id</span><span class="sxs-lookup"><span data-stu-id="69588-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="69588-119">-確認</span><span class="sxs-lookup"><span data-stu-id="69588-119">-Confirm</span></span>
<span data-ttu-id="69588-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="69588-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69588-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69588-121">-WhatIf</span></span>
<span data-ttu-id="69588-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69588-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69588-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69588-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69588-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69588-124">CommonParameters</span></span>
<span data-ttu-id="69588-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="69588-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69588-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="69588-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69588-127">輸入</span><span class="sxs-lookup"><span data-stu-id="69588-127">INPUTS</span></span>

### <span data-ttu-id="69588-128">System.String</span><span class="sxs-lookup"><span data-stu-id="69588-128">System.String</span></span>

## <span data-ttu-id="69588-129">輸出</span><span class="sxs-lookup"><span data-stu-id="69588-129">OUTPUTS</span></span>

### <span data-ttu-id="69588-130">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="69588-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="69588-131">筆記</span><span class="sxs-lookup"><span data-stu-id="69588-131">NOTES</span></span>

## <span data-ttu-id="69588-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="69588-132">RELATED LINKS</span></span>
