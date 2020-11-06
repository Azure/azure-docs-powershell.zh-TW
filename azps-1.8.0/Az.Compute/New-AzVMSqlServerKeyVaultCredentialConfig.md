---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: ec67022ff40247deb7d1ebc7e28bf7e1654fbd99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622746"
---
# <span data-ttu-id="a8298-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="a8298-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="a8298-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8298-102">SYNOPSIS</span></span>
<span data-ttu-id="a8298-103">針對虛擬機器上的 SQL server 金鑰保存庫認證建立一個 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="a8298-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="a8298-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8298-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8298-105">說明</span><span class="sxs-lookup"><span data-stu-id="a8298-105">DESCRIPTION</span></span>

## <span data-ttu-id="a8298-106">示例</span><span class="sxs-lookup"><span data-stu-id="a8298-106">EXAMPLES</span></span>

## <span data-ttu-id="a8298-107">參數</span><span class="sxs-lookup"><span data-stu-id="a8298-107">PARAMETERS</span></span>

### <span data-ttu-id="a8298-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="a8298-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="a8298-109">Azure 金鑰保存庫服務 URL</span><span class="sxs-lookup"><span data-stu-id="a8298-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="a8298-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="a8298-110">-CredentialName</span></span>
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

### <span data-ttu-id="a8298-111">-啟用</span><span class="sxs-lookup"><span data-stu-id="a8298-111">-Enable</span></span>
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

### <span data-ttu-id="a8298-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8298-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="a8298-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a8298-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="a8298-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="a8298-114">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="a8298-115">-確認</span><span class="sxs-lookup"><span data-stu-id="a8298-115">-Confirm</span></span>
<span data-ttu-id="a8298-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a8298-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8298-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8298-117">-WhatIf</span></span>
<span data-ttu-id="a8298-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8298-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8298-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8298-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8298-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8298-120">CommonParameters</span></span>
<span data-ttu-id="a8298-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8298-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8298-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8298-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8298-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a8298-123">INPUTS</span></span>

### <span data-ttu-id="a8298-124">System.object</span><span class="sxs-lookup"><span data-stu-id="a8298-124">System.String</span></span>

### <span data-ttu-id="a8298-125">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="a8298-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a8298-126">SecureString</span><span class="sxs-lookup"><span data-stu-id="a8298-126">System.Security.SecureString</span></span>

## <span data-ttu-id="a8298-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a8298-127">OUTPUTS</span></span>

### <span data-ttu-id="a8298-128">KeyVaultCredentialSettings 的計算。</span><span class="sxs-lookup"><span data-stu-id="a8298-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="a8298-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a8298-129">NOTES</span></span>

## <span data-ttu-id="a8298-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8298-130">RELATED LINKS</span></span>
