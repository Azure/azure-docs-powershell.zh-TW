---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: ecb49271c49e441140a43f8cb8ae5d65be56cd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625398"
---
# <span data-ttu-id="e1b51-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e1b51-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="e1b51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1b51-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b51-103">取得透明的資料加密 (TDE) 保護器</span><span class="sxs-lookup"><span data-stu-id="e1b51-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1b51-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1b51-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1b51-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1b51-105">DESCRIPTION</span></span>
<span data-ttu-id="e1b51-106">Get-AzureRmSqlServerTransparentDataEncryptionProtector Cmdlet 會取得 TDE 保護程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e1b51-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="e1b51-107">示例</span><span class="sxs-lookup"><span data-stu-id="e1b51-107">EXAMPLES</span></span>

### <span data-ttu-id="e1b51-108">範例1：取得透明的資料加密 (TDE) 保護器</span><span class="sxs-lookup"><span data-stu-id="e1b51-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="e1b51-109">這個命令會取得名為 ContosoResourceGroup 之資源群組中名為 ContosoServer 之伺服器的 TDE 保護器。</span><span class="sxs-lookup"><span data-stu-id="e1b51-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>

<span data-ttu-id="e1b51-110">ResourceGroupName ServerName 類型 ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="e1b51-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="e1b51-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="e1b51-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="e1b51-112">參數</span><span class="sxs-lookup"><span data-stu-id="e1b51-112">PARAMETERS</span></span>

### <span data-ttu-id="e1b51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b51-113">-DefaultProfile</span></span>
<span data-ttu-id="e1b51-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e1b51-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1b51-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1b51-115">-ResourceGroupName</span></span>
<span data-ttu-id="e1b51-116">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="e1b51-116">The name of the resource group</span></span>

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

### <span data-ttu-id="e1b51-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e1b51-117">-ServerName</span></span>
<span data-ttu-id="e1b51-118">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="e1b51-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="e1b51-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e1b51-119">-Confirm</span></span>
<span data-ttu-id="e1b51-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1b51-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1b51-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1b51-121">-WhatIf</span></span>
<span data-ttu-id="e1b51-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1b51-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1b51-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1b51-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1b51-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b51-124">CommonParameters</span></span>
<span data-ttu-id="e1b51-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1b51-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b51-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1b51-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b51-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e1b51-127">INPUTS</span></span>

### <span data-ttu-id="e1b51-128">System.object</span><span class="sxs-lookup"><span data-stu-id="e1b51-128">System.String</span></span>

## <span data-ttu-id="e1b51-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e1b51-129">OUTPUTS</span></span>

### <span data-ttu-id="e1b51-130">System.object</span><span class="sxs-lookup"><span data-stu-id="e1b51-130">System.Object</span></span>

## <span data-ttu-id="e1b51-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e1b51-131">NOTES</span></span>

## <span data-ttu-id="e1b51-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1b51-132">RELATED LINKS</span></span>

[<span data-ttu-id="e1b51-133">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="e1b51-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
