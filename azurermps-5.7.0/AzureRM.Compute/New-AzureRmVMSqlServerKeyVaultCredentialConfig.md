---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 4e252001d1459c52a35b766d34c91050df62073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448751"
---
# <span data-ttu-id="a1b96-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="a1b96-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="a1b96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1b96-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b96-103">針對虛擬機器上的 SQL server 金鑰保存庫認證建立一個 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="a1b96-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1b96-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1b96-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1b96-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1b96-105">DESCRIPTION</span></span>

## <span data-ttu-id="a1b96-106">示例</span><span class="sxs-lookup"><span data-stu-id="a1b96-106">EXAMPLES</span></span>

## <span data-ttu-id="a1b96-107">參數</span><span class="sxs-lookup"><span data-stu-id="a1b96-107">PARAMETERS</span></span>

### <span data-ttu-id="a1b96-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="a1b96-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="a1b96-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="a1b96-109">-CredentialName</span></span>
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

### <span data-ttu-id="a1b96-110">-啟用</span><span class="sxs-lookup"><span data-stu-id="a1b96-110">-Enable</span></span>
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

### <span data-ttu-id="a1b96-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b96-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="a1b96-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a1b96-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="a1b96-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="a1b96-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="a1b96-114">-確認</span><span class="sxs-lookup"><span data-stu-id="a1b96-114">-Confirm</span></span>
<span data-ttu-id="a1b96-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a1b96-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b96-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b96-116">-WhatIf</span></span>
<span data-ttu-id="a1b96-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1b96-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a1b96-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1b96-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b96-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b96-119">CommonParameters</span></span>
<span data-ttu-id="a1b96-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1b96-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b96-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1b96-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b96-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a1b96-122">INPUTS</span></span>

### <span data-ttu-id="a1b96-123">所有</span><span class="sxs-lookup"><span data-stu-id="a1b96-123">None</span></span>
<span data-ttu-id="a1b96-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a1b96-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1b96-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a1b96-125">OUTPUTS</span></span>

## <span data-ttu-id="a1b96-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a1b96-126">NOTES</span></span>

## <span data-ttu-id="a1b96-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1b96-127">RELATED LINKS</span></span>

