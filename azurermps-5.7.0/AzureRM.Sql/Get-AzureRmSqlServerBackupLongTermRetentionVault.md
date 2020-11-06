---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 567cb47599a23bf83581afb97a425902ee0e159a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447622"
---
# <span data-ttu-id="4fed5-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="4fed5-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="4fed5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4fed5-102">SYNOPSIS</span></span>
<span data-ttu-id="4fed5-103">取得伺服器長保留期保存庫。</span><span class="sxs-lookup"><span data-stu-id="4fed5-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fed5-104">句法</span><span class="sxs-lookup"><span data-stu-id="4fed5-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fed5-105">說明</span><span class="sxs-lookup"><span data-stu-id="4fed5-105">DESCRIPTION</span></span>
<span data-ttu-id="4fed5-106">**AzureRmSqlServerBackupLongTermRetentionVault** Cmdlet 會取得已登錄至此伺服器的長期保留式保險存儲區。</span><span class="sxs-lookup"><span data-stu-id="4fed5-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="4fed5-107">Vault 是用來儲存備份資料的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="4fed5-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="4fed5-108">示例</span><span class="sxs-lookup"><span data-stu-id="4fed5-108">EXAMPLES</span></span>

## <span data-ttu-id="4fed5-109">參數</span><span class="sxs-lookup"><span data-stu-id="4fed5-109">PARAMETERS</span></span>

### <span data-ttu-id="4fed5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fed5-110">-DefaultProfile</span></span>
<span data-ttu-id="4fed5-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4fed5-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fed5-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fed5-112">-ResourceGroupName</span></span>
<span data-ttu-id="4fed5-113">指定包含伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fed5-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="4fed5-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4fed5-114">-ServerName</span></span>
<span data-ttu-id="4fed5-115">指定此 Cmdlet 取得其電子倉庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="4fed5-115">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="4fed5-116">-確認</span><span class="sxs-lookup"><span data-stu-id="4fed5-116">-Confirm</span></span>
<span data-ttu-id="4fed5-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4fed5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fed5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fed5-118">-WhatIf</span></span>
<span data-ttu-id="4fed5-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4fed5-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fed5-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4fed5-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fed5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fed5-121">CommonParameters</span></span>
<span data-ttu-id="4fed5-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4fed5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fed5-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4fed5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fed5-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4fed5-124">INPUTS</span></span>

### <span data-ttu-id="4fed5-125">所有</span><span class="sxs-lookup"><span data-stu-id="4fed5-125">None</span></span>
<span data-ttu-id="4fed5-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4fed5-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4fed5-127">輸出</span><span class="sxs-lookup"><span data-stu-id="4fed5-127">OUTPUTS</span></span>

## <span data-ttu-id="4fed5-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4fed5-128">NOTES</span></span>

## <span data-ttu-id="4fed5-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fed5-129">RELATED LINKS</span></span>

[<span data-ttu-id="4fed5-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="4fed5-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="4fed5-131">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="4fed5-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

