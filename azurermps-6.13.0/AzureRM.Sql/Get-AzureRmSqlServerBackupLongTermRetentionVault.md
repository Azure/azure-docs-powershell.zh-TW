---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 0aeee8e991d0f74a341a750e69016b12027fe584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449709"
---
# <span data-ttu-id="9200a-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="9200a-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="9200a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9200a-102">SYNOPSIS</span></span>
<span data-ttu-id="9200a-103">取得伺服器長保留期保存庫。</span><span class="sxs-lookup"><span data-stu-id="9200a-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9200a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9200a-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9200a-105">說明</span><span class="sxs-lookup"><span data-stu-id="9200a-105">DESCRIPTION</span></span>
<span data-ttu-id="9200a-106">**AzureRmSqlServerBackupLongTermRetentionVault** Cmdlet 會取得已登錄至此伺服器的長期保留式保險存儲區。</span><span class="sxs-lookup"><span data-stu-id="9200a-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="9200a-107">Vault 是用來儲存備份資料的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="9200a-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="9200a-108">示例</span><span class="sxs-lookup"><span data-stu-id="9200a-108">EXAMPLES</span></span>

## <span data-ttu-id="9200a-109">參數</span><span class="sxs-lookup"><span data-stu-id="9200a-109">PARAMETERS</span></span>

### <span data-ttu-id="9200a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9200a-110">-DefaultProfile</span></span>
<span data-ttu-id="9200a-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9200a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9200a-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9200a-112">-ResourceGroupName</span></span>
<span data-ttu-id="9200a-113">指定包含伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9200a-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="9200a-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9200a-114">-ServerName</span></span>
<span data-ttu-id="9200a-115">指定此 Cmdlet 取得其電子倉庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9200a-115">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="9200a-116">-確認</span><span class="sxs-lookup"><span data-stu-id="9200a-116">-Confirm</span></span>
<span data-ttu-id="9200a-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9200a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9200a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9200a-118">-WhatIf</span></span>
<span data-ttu-id="9200a-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9200a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9200a-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9200a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9200a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9200a-121">CommonParameters</span></span>
<span data-ttu-id="9200a-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9200a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9200a-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9200a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9200a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="9200a-124">INPUTS</span></span>

### <span data-ttu-id="9200a-125">System.object</span><span class="sxs-lookup"><span data-stu-id="9200a-125">System.String</span></span>

## <span data-ttu-id="9200a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="9200a-126">OUTPUTS</span></span>

### <span data-ttu-id="9200a-127">AzureSqlServerBackupLongTermRetentionVaultModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="9200a-127">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="9200a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="9200a-128">NOTES</span></span>

## <span data-ttu-id="9200a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="9200a-129">RELATED LINKS</span></span>

[<span data-ttu-id="9200a-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="9200a-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="9200a-131">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="9200a-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

