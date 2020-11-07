---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: dc1ea08b0770c7438574d4ef2cc6a97cb99f2909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624441"
---
# <span data-ttu-id="f8ca8-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="f8ca8-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="f8ca8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ca8-103">針對虛擬機器上的 SQL server 金鑰保存庫認證建立一個 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="f8ca8-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8ca8-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8ca8-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8ca8-105">說明</span><span class="sxs-lookup"><span data-stu-id="f8ca8-105">DESCRIPTION</span></span>

## <span data-ttu-id="f8ca8-106">示例</span><span class="sxs-lookup"><span data-stu-id="f8ca8-106">EXAMPLES</span></span>

## <span data-ttu-id="f8ca8-107">參數</span><span class="sxs-lookup"><span data-stu-id="f8ca8-107">PARAMETERS</span></span>

### <span data-ttu-id="f8ca8-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="f8ca8-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="f8ca8-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="f8ca8-109">-CredentialName</span></span>
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

### <span data-ttu-id="f8ca8-110">-啟用</span><span class="sxs-lookup"><span data-stu-id="f8ca8-110">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ca8-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8ca8-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f8ca8-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f8ca8-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="f8ca8-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="f8ca8-113">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ca8-114">-確認</span><span class="sxs-lookup"><span data-stu-id="f8ca8-114">-Confirm</span></span>
<span data-ttu-id="f8ca8-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f8ca8-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ca8-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8ca8-116">-WhatIf</span></span>
<span data-ttu-id="f8ca8-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8ca8-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8ca8-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8ca8-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ca8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ca8-119">CommonParameters</span></span>
<span data-ttu-id="f8ca8-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8ca8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ca8-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8ca8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ca8-122">輸入</span><span class="sxs-lookup"><span data-stu-id="f8ca8-122">INPUTS</span></span>

### <span data-ttu-id="f8ca8-123">System.object</span><span class="sxs-lookup"><span data-stu-id="f8ca8-123">System.String</span></span>

### <span data-ttu-id="f8ca8-124">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f8ca8-124">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f8ca8-125">SecureString</span><span class="sxs-lookup"><span data-stu-id="f8ca8-125">System.Security.SecureString</span></span>

## <span data-ttu-id="f8ca8-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f8ca8-126">OUTPUTS</span></span>

### <span data-ttu-id="f8ca8-127">KeyVaultCredentialSettings 的計算。</span><span class="sxs-lookup"><span data-stu-id="f8ca8-127">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="f8ca8-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f8ca8-128">NOTES</span></span>

## <span data-ttu-id="f8ca8-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8ca8-129">RELATED LINKS</span></span>
