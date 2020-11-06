---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: b05158ae21219760c9c88fe9c0ae3e4978b76f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448447"
---
# <span data-ttu-id="d061e-101">Set-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d061e-101">Set-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="d061e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d061e-102">SYNOPSIS</span></span>
<span data-ttu-id="d061e-103">在指定的 Data Lake Store 中修改指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="d061e-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d061e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d061e-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d061e-105">說明</span><span class="sxs-lookup"><span data-stu-id="d061e-105">DESCRIPTION</span></span>
<span data-ttu-id="d061e-106">**AzureRmDataLakeStoreVirtualNetworkRule** Cmdlet 會修改指定資料 Lake store 中指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="d061e-106">The **Set-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d061e-107">示例</span><span class="sxs-lookup"><span data-stu-id="d061e-107">EXAMPLES</span></span>

### <span data-ttu-id="d061e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d061e-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="d061e-109">將帳戶 "dl" 中的虛擬網路規則 "myVNET" 的子網 id 更新為 "updatedId"</span><span class="sxs-lookup"><span data-stu-id="d061e-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="d061e-110">參數</span><span class="sxs-lookup"><span data-stu-id="d061e-110">PARAMETERS</span></span>

### <span data-ttu-id="d061e-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="d061e-111">-Account</span></span>
<span data-ttu-id="d061e-112">要在其中更新虛擬網路規則的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="d061e-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="d061e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d061e-113">-DefaultProfile</span></span>
<span data-ttu-id="d061e-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d061e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d061e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d061e-115">-Name</span></span>
<span data-ttu-id="d061e-116">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d061e-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="d061e-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d061e-117">-SubnetId</span></span>
<span data-ttu-id="d061e-118">虛擬網路規則的有效 ip 範圍起始</span><span class="sxs-lookup"><span data-stu-id="d061e-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="d061e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d061e-119">-Confirm</span></span>
<span data-ttu-id="d061e-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d061e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d061e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d061e-121">-WhatIf</span></span>
<span data-ttu-id="d061e-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d061e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d061e-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d061e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d061e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d061e-124">CommonParameters</span></span>
<span data-ttu-id="d061e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d061e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d061e-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d061e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d061e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d061e-127">INPUTS</span></span>

### <span data-ttu-id="d061e-128">System.object</span><span class="sxs-lookup"><span data-stu-id="d061e-128">System.String</span></span>

## <span data-ttu-id="d061e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d061e-129">OUTPUTS</span></span>

### <span data-ttu-id="d061e-130">DataLakeStoreVirtualNetworkRule 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="d061e-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="d061e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d061e-131">NOTES</span></span>

## <span data-ttu-id="d061e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d061e-132">RELATED LINKS</span></span>
