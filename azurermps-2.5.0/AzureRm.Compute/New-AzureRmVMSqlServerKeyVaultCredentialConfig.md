---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
ms.openlocfilehash: ee627065d1d6be8037d1a9b054ec6452b9becb41
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801774"
---
# <span data-ttu-id="dae42-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="dae42-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="dae42-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dae42-102">SYNOPSIS</span></span>
<span data-ttu-id="dae42-103">針對虛擬機器上的 SQL server 金鑰保存庫認證建立一個 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="dae42-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dae42-104">句法</span><span class="sxs-lookup"><span data-stu-id="dae42-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dae42-105">說明</span><span class="sxs-lookup"><span data-stu-id="dae42-105">DESCRIPTION</span></span>

## <span data-ttu-id="dae42-106">示例</span><span class="sxs-lookup"><span data-stu-id="dae42-106">EXAMPLES</span></span>

## <span data-ttu-id="dae42-107">參數</span><span class="sxs-lookup"><span data-stu-id="dae42-107">PARAMETERS</span></span>

### <span data-ttu-id="dae42-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="dae42-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="dae42-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-110">-啟用</span><span class="sxs-lookup"><span data-stu-id="dae42-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dae42-111">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dae42-112">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="dae42-113">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-114">-確認</span><span class="sxs-lookup"><span data-stu-id="dae42-114">-Confirm</span></span>
<span data-ttu-id="dae42-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dae42-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dae42-116">-WhatIf</span></span>
<span data-ttu-id="dae42-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dae42-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="dae42-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dae42-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae42-119">CommonParameters</span></span>
<span data-ttu-id="dae42-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dae42-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae42-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dae42-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae42-122">輸入</span><span class="sxs-lookup"><span data-stu-id="dae42-122">INPUTS</span></span>

### <span data-ttu-id="dae42-123">所有</span><span class="sxs-lookup"><span data-stu-id="dae42-123">None</span></span>
<span data-ttu-id="dae42-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="dae42-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dae42-125">輸出</span><span class="sxs-lookup"><span data-stu-id="dae42-125">OUTPUTS</span></span>

### <span data-ttu-id="dae42-126">KeyVaultCredentialSettings 的計算。</span><span class="sxs-lookup"><span data-stu-id="dae42-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="dae42-127">筆記</span><span class="sxs-lookup"><span data-stu-id="dae42-127">NOTES</span></span>

## <span data-ttu-id="dae42-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="dae42-128">RELATED LINKS</span></span>

