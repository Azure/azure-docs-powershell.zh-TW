---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: e76ba16f9578eefdce36a1f3d726e027be2a9ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455915"
---
# <span data-ttu-id="f7e3b-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="f7e3b-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="f7e3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e3b-103">設定伺服器的長期保留保險存儲區。</span><span class="sxs-lookup"><span data-stu-id="f7e3b-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7e3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7e3b-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7e3b-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7e3b-105">DESCRIPTION</span></span>
<span data-ttu-id="f7e3b-106">**AzureRmSqlServerBackupLongTermRetentionVault** Cmdlet 會設定在此伺服器上註冊長期保留式保險存儲區。</span><span class="sxs-lookup"><span data-stu-id="f7e3b-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="f7e3b-107">Vault 是用來儲存備份資料的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="f7e3b-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="f7e3b-108">示例</span><span class="sxs-lookup"><span data-stu-id="f7e3b-108">EXAMPLES</span></span>

## <span data-ttu-id="f7e3b-109">參數</span><span class="sxs-lookup"><span data-stu-id="f7e3b-109">PARAMETERS</span></span>

### <span data-ttu-id="f7e3b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e3b-110">-DefaultProfile</span></span>
<span data-ttu-id="f7e3b-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f7e3b-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7e3b-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7e3b-112">-ResourceGroupName</span></span>
<span data-ttu-id="f7e3b-113">指定包含伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7e3b-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="f7e3b-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7e3b-114">-ResourceId</span></span>
<span data-ttu-id="f7e3b-115">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7e3b-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7e3b-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f7e3b-116">-ServerName</span></span>
<span data-ttu-id="f7e3b-117">指定此 Cmdlet 為其設定電子倉庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="f7e3b-117">Specifies the server for which this cmdlet sets a vault.</span></span>

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

### <span data-ttu-id="f7e3b-118">-確認</span><span class="sxs-lookup"><span data-stu-id="f7e3b-118">-Confirm</span></span>
<span data-ttu-id="f7e3b-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7e3b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7e3b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7e3b-120">-WhatIf</span></span>
<span data-ttu-id="f7e3b-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7e3b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7e3b-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7e3b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7e3b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e3b-123">CommonParameters</span></span>
<span data-ttu-id="f7e3b-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7e3b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e3b-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7e3b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e3b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f7e3b-126">INPUTS</span></span>

### <span data-ttu-id="f7e3b-127">System.object</span><span class="sxs-lookup"><span data-stu-id="f7e3b-127">System.String</span></span>

## <span data-ttu-id="f7e3b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f7e3b-128">OUTPUTS</span></span>

### <span data-ttu-id="f7e3b-129">AzureSqlServerBackupLongTermRetentionVaultModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="f7e3b-129">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="f7e3b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f7e3b-130">NOTES</span></span>

## <span data-ttu-id="f7e3b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7e3b-131">RELATED LINKS</span></span>

[<span data-ttu-id="f7e3b-132">AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="f7e3b-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="f7e3b-133">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="f7e3b-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
