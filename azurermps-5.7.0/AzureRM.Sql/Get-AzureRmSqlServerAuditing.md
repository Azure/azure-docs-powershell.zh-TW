---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 636b3602c6dafc2c00e02e19aa35d0e91c278137
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447625"
---
# <span data-ttu-id="11943-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="11943-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="11943-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11943-102">SYNOPSIS</span></span>
<span data-ttu-id="11943-103">取得 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="11943-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11943-104">句法</span><span class="sxs-lookup"><span data-stu-id="11943-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11943-105">說明</span><span class="sxs-lookup"><span data-stu-id="11943-105">DESCRIPTION</span></span>
<span data-ttu-id="11943-106">**AzureRmSqlServerAuditing** Cmdlet 會取得 Azure SQL server 的 blob 審核原則。</span><span class="sxs-lookup"><span data-stu-id="11943-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="11943-107">指定 *ResourceGroupName* 和 *ServerName* 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="11943-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="11943-108">這個 Cmdlet 會傳回在指定的 Azure SQL server 中定義的 Azure SQL 資料庫所使用的原則。</span><span class="sxs-lookup"><span data-stu-id="11943-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="11943-109">示例</span><span class="sxs-lookup"><span data-stu-id="11943-109">EXAMPLES</span></span>

### <span data-ttu-id="11943-110">範例1：取得 Azure SQL server 的審核設定</span><span class="sxs-lookup"><span data-stu-id="11943-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="11943-111">參數</span><span class="sxs-lookup"><span data-stu-id="11943-111">PARAMETERS</span></span>

### <span data-ttu-id="11943-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11943-112">-DefaultProfile</span></span>
<span data-ttu-id="11943-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="11943-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11943-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11943-114">-ResourceGroupName</span></span>
<span data-ttu-id="11943-115">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11943-115">The name of the resource group.</span></span>

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

### <span data-ttu-id="11943-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="11943-116">-ServerName</span></span>
<span data-ttu-id="11943-117">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="11943-117">SQL server name.</span></span>

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

### <span data-ttu-id="11943-118">-確認</span><span class="sxs-lookup"><span data-stu-id="11943-118">-Confirm</span></span>
<span data-ttu-id="11943-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11943-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11943-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11943-120">-WhatIf</span></span>
<span data-ttu-id="11943-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11943-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11943-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11943-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11943-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11943-123">CommonParameters</span></span>
<span data-ttu-id="11943-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11943-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11943-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11943-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11943-126">輸入</span><span class="sxs-lookup"><span data-stu-id="11943-126">INPUTS</span></span>

### <span data-ttu-id="11943-127">所有</span><span class="sxs-lookup"><span data-stu-id="11943-127">None</span></span>
<span data-ttu-id="11943-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="11943-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11943-129">輸出</span><span class="sxs-lookup"><span data-stu-id="11943-129">OUTPUTS</span></span>

### <span data-ttu-id="11943-130">ServerBlobAuditingSettingsModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="11943-130">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="11943-131">筆記</span><span class="sxs-lookup"><span data-stu-id="11943-131">NOTES</span></span>

## <span data-ttu-id="11943-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="11943-132">RELATED LINKS</span></span>
