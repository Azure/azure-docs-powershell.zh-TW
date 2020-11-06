---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 3ad3e98e6fb2ab5c6e0b04495142861ecfe9e0ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450627"
---
# <span data-ttu-id="9fbc6-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9fbc6-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="9fbc6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9fbc6-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbc6-103">修改指定資料 Lake Store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="9fbc6-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fbc6-104">句法</span><span class="sxs-lookup"><span data-stu-id="9fbc6-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fbc6-105">說明</span><span class="sxs-lookup"><span data-stu-id="9fbc6-105">DESCRIPTION</span></span>
<span data-ttu-id="9fbc6-106">**AzureRmDataLakeStoreFirewallRule** Cmdlet 會修改指定資料 Lake store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="9fbc6-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="9fbc6-107">示例</span><span class="sxs-lookup"><span data-stu-id="9fbc6-107">EXAMPLES</span></span>

### <span data-ttu-id="9fbc6-108">範例1：更新防火牆規則的開始和結束 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="9fbc6-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="9fbc6-109">更新帳戶 "ContosoADL" 中的防火牆規則 "MyFirewallRule" 以包含127.0.0.1 範圍（127.0.0.1）127.0.0。2</span><span class="sxs-lookup"><span data-stu-id="9fbc6-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="9fbc6-110">參數</span><span class="sxs-lookup"><span data-stu-id="9fbc6-110">PARAMETERS</span></span>

### <span data-ttu-id="9fbc6-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="9fbc6-111">-Account</span></span>
<span data-ttu-id="9fbc6-112">要在其中更新防火牆規則的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="9fbc6-112">The Data Lake Store account to update the firewall rule in</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fbc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbc6-113">-DefaultProfile</span></span>
<span data-ttu-id="9fbc6-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9fbc6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fbc6-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="9fbc6-115">-EndIpAddress</span></span>
<span data-ttu-id="9fbc6-116">防火牆規則有效 ip 範圍的結尾</span><span class="sxs-lookup"><span data-stu-id="9fbc6-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fbc6-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9fbc6-117">-Name</span></span>
<span data-ttu-id="9fbc6-118">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fbc6-118">The name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fbc6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fbc6-119">-ResourceGroupName</span></span>
<span data-ttu-id="9fbc6-120">指定包含要更新防火牆規則之帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fbc6-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fbc6-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="9fbc6-121">-StartIpAddress</span></span>
<span data-ttu-id="9fbc6-122">防火牆規則的有效 ip 範圍起點</span><span class="sxs-lookup"><span data-stu-id="9fbc6-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fbc6-123">-確認</span><span class="sxs-lookup"><span data-stu-id="9fbc6-123">-Confirm</span></span>
<span data-ttu-id="9fbc6-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9fbc6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fbc6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fbc6-125">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fbc6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbc6-126">CommonParameters</span></span>
<span data-ttu-id="9fbc6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9fbc6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbc6-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9fbc6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbc6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9fbc6-129">INPUTS</span></span>

### <span data-ttu-id="9fbc6-130">所有</span><span class="sxs-lookup"><span data-stu-id="9fbc6-130">None</span></span>
<span data-ttu-id="9fbc6-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9fbc6-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fbc6-132">輸出</span><span class="sxs-lookup"><span data-stu-id="9fbc6-132">OUTPUTS</span></span>

### <span data-ttu-id="9fbc6-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9fbc6-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="9fbc6-134">更新的防火牆規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9fbc6-134">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="9fbc6-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9fbc6-135">NOTES</span></span>

## <span data-ttu-id="9fbc6-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fbc6-136">RELATED LINKS</span></span>

