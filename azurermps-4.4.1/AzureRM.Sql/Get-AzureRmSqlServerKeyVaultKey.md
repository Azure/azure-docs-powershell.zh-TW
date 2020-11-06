---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 17022a34ad8a5f2be673243e9dcb6c7063c8fbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447919"
---
# <span data-ttu-id="11354-101">Get-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11354-101">Get-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="11354-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11354-102">SYNOPSIS</span></span>
<span data-ttu-id="11354-103">取得 SQL server 的主要保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="11354-103">Gets a SQL server's Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11354-104">句法</span><span class="sxs-lookup"><span data-stu-id="11354-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11354-105">說明</span><span class="sxs-lookup"><span data-stu-id="11354-105">DESCRIPTION</span></span>
<span data-ttu-id="11354-106">Get-AzureRmSqlServerKeyVaultKey Cmdlet 會取得有關 SQL server 上的主要保存庫金鑰的資訊。</span><span class="sxs-lookup"><span data-stu-id="11354-106">The Get-AzureRmSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="11354-107">您可以透過提供 KeyId 來查看伺服器上的所有金鑰，或查看特定的金鑰。</span><span class="sxs-lookup"><span data-stu-id="11354-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="11354-108">示例</span><span class="sxs-lookup"><span data-stu-id="11354-108">EXAMPLES</span></span>

### <span data-ttu-id="11354-109">--------------------------範例1：取得所有的主要保存庫金鑰--------------------------</span><span class="sxs-lookup"><span data-stu-id="11354-109">--------------------------  Example 1: Get all Key Vault keys  --------------------------</span></span>
```
PS C:\> Get-AzureRmSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="11354-110">這個命令會取得 SQL server 上的所有主要保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="11354-110">This command gets all the Key Vault keys on a SQL server.</span></span>

<span data-ttu-id="11354-111">ResourceGroupName： ContosoResourceGroup ServerName： ContosoServer ServerKeyName： contoso_contosokey_01234567890123456789012345678901 類型： AzureKeyVault Uri： https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 指紋： 1122334455667788990011223344556677889900 CreationDate： 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="11354-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

<span data-ttu-id="11354-112">ResourceGroupName： ContosoResourceGroup ServerName： ContosoServer ServerKeyName： contoso_contosokey2_01234567890123456789012345678901 類型： AzureKeyVault Uri： https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 指紋： 0099887766554433221100998877665544332211 CreationDate： 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="11354-112">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="11354-113">--------------------------範例2：取得特定的金鑰保存庫金鑰--------------------------</span><span class="sxs-lookup"><span data-stu-id="11354-113">--------------------------  Example 2: Get a specific Key Vault key  --------------------------</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="11354-114">這個命令會取得 Id 為 "" 的主要保存庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ，然後將它儲存在 $MyServerKeyVaultKey 變數中。</span><span class="sxs-lookup"><span data-stu-id="11354-114">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="11354-115">您可以檢查 $MyServerKeyVaultKey 的屬性，以取得關於主要電子倉庫的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="11354-115">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="11354-116">參數</span><span class="sxs-lookup"><span data-stu-id="11354-116">PARAMETERS</span></span>

### <span data-ttu-id="11354-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="11354-117">-KeyId</span></span>
<span data-ttu-id="11354-118">Azure 金鑰保存庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="11354-118">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11354-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11354-119">-ResourceGroupName</span></span>
<span data-ttu-id="11354-120">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="11354-120">The name of the resource group</span></span>

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

### <span data-ttu-id="11354-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="11354-121">-ServerName</span></span>
<span data-ttu-id="11354-122">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="11354-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="11354-123">-確認</span><span class="sxs-lookup"><span data-stu-id="11354-123">-Confirm</span></span>
<span data-ttu-id="11354-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11354-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11354-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11354-125">-WhatIf</span></span>
<span data-ttu-id="11354-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11354-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11354-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11354-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11354-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11354-128">-DefaultProfile</span></span>
<span data-ttu-id="11354-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11354-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11354-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11354-130">CommonParameters</span></span>
<span data-ttu-id="11354-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11354-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11354-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11354-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11354-133">輸入</span><span class="sxs-lookup"><span data-stu-id="11354-133">INPUTS</span></span>

### <span data-ttu-id="11354-134">System.object</span><span class="sxs-lookup"><span data-stu-id="11354-134">System.String</span></span>

## <span data-ttu-id="11354-135">輸出</span><span class="sxs-lookup"><span data-stu-id="11354-135">OUTPUTS</span></span>

### <span data-ttu-id="11354-136">System.object</span><span class="sxs-lookup"><span data-stu-id="11354-136">System.Object</span></span>

## <span data-ttu-id="11354-137">筆記</span><span class="sxs-lookup"><span data-stu-id="11354-137">NOTES</span></span>

## <span data-ttu-id="11354-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="11354-138">RELATED LINKS</span></span>

[<span data-ttu-id="11354-139">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="11354-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
