---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: e8606f9eecfac63b68e9b8a26ecbebb89431e509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623631"
---
# <span data-ttu-id="37c0c-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="37c0c-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="37c0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="37c0c-103">從 SQL server 移除金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="37c0c-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37c0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="37c0c-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37c0c-105">說明</span><span class="sxs-lookup"><span data-stu-id="37c0c-105">DESCRIPTION</span></span>
<span data-ttu-id="37c0c-106">Remove-AzureRmSqlServerKeyVaultKey Cmdlet 會從指定的 SQL server 中移除金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="37c0c-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>

<span data-ttu-id="37c0c-107">請注意，不會變更 SQL server 對金鑰電子倉庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="37c0c-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="37c0c-108">若要變更許可權，請使用 [設定-AzureRmKeyVaultAccessPolicy]。</span><span class="sxs-lookup"><span data-stu-id="37c0c-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>

<span data-ttu-id="37c0c-109">請注意，這個 Cmdlet 不會變更金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="37c0c-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="37c0c-110">若要從 [主要電子倉庫] 移除金鑰，請使用 [移除-AzureKeyVaultKey]。</span><span class="sxs-lookup"><span data-stu-id="37c0c-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="37c0c-111">示例</span><span class="sxs-lookup"><span data-stu-id="37c0c-111">EXAMPLES</span></span>

### <span data-ttu-id="37c0c-112">--------------------------範例1：移除金鑰保存庫金鑰--------------------------</span><span class="sxs-lookup"><span data-stu-id="37c0c-112">--------------------------  Example 1: Remove a Key Vault key  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="37c0c-113">這個命令會從指定的伺服器移除 Id 為 '」的主要保存庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 。</span><span class="sxs-lookup"><span data-stu-id="37c0c-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>

<span data-ttu-id="37c0c-114">ResourceGroupName： ContosoResourceGroup ServerName： ContosoServer ServerKeyName： contoso_contosokey_01234567890123456789012345678901 類型： AzureKeyVault Uri： https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 指紋： 1122334455667788990011223344556677889900 CreationDate： 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="37c0c-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="37c0c-115">參數</span><span class="sxs-lookup"><span data-stu-id="37c0c-115">PARAMETERS</span></span>

### <span data-ttu-id="37c0c-116">-KeyId</span><span class="sxs-lookup"><span data-stu-id="37c0c-116">-KeyId</span></span>
<span data-ttu-id="37c0c-117">Azure 金鑰保存庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="37c0c-117">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="37c0c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37c0c-118">-ResourceGroupName</span></span>
<span data-ttu-id="37c0c-119">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="37c0c-119">The name of the resource group</span></span>

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

### <span data-ttu-id="37c0c-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="37c0c-120">-ServerName</span></span>
<span data-ttu-id="37c0c-121">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="37c0c-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="37c0c-122">-確認</span><span class="sxs-lookup"><span data-stu-id="37c0c-122">-Confirm</span></span>
<span data-ttu-id="37c0c-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="37c0c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37c0c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c0c-124">-WhatIf</span></span>
<span data-ttu-id="37c0c-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37c0c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37c0c-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37c0c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37c0c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c0c-127">-DefaultProfile</span></span>
<span data-ttu-id="37c0c-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37c0c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37c0c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c0c-129">CommonParameters</span></span>
<span data-ttu-id="37c0c-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37c0c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c0c-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="37c0c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c0c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="37c0c-132">INPUTS</span></span>

### <span data-ttu-id="37c0c-133">System.object</span><span class="sxs-lookup"><span data-stu-id="37c0c-133">System.String</span></span>

## <span data-ttu-id="37c0c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="37c0c-134">OUTPUTS</span></span>

### <span data-ttu-id="37c0c-135">System.object</span><span class="sxs-lookup"><span data-stu-id="37c0c-135">System.Object</span></span>

## <span data-ttu-id="37c0c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="37c0c-136">NOTES</span></span>

## <span data-ttu-id="37c0c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="37c0c-137">RELATED LINKS</span></span>

[<span data-ttu-id="37c0c-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="37c0c-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
