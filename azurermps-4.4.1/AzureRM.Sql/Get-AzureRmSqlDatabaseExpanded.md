---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
ms.openlocfilehash: 56254dc295b650012cdff321f4f6e77054614186
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456355"
---
# <span data-ttu-id="4ecc1-101">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="4ecc1-101">Get-AzureRmSqlDatabaseExpanded</span></span>

## <span data-ttu-id="4ecc1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ecc1-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecc1-103">取得資料庫及其展開的屬性值。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-103">Gets a database and its expanded property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ecc1-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ecc1-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ecc1-105">說明</span><span class="sxs-lookup"><span data-stu-id="4ecc1-105">DESCRIPTION</span></span>
<span data-ttu-id="4ecc1-106">**AzureRmSqlDatabaseExpanded** Cmdlet 會取得資料庫及其展開的屬性值。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-106">The **Get-AzureRmSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>

<span data-ttu-id="4ecc1-107">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4ecc1-108">示例</span><span class="sxs-lookup"><span data-stu-id="4ecc1-108">EXAMPLES</span></span>

### <span data-ttu-id="4ecc1-109">範例1：取得擁有 service 層 advisor 資訊的資料庫物件</span><span class="sxs-lookup"><span data-stu-id="4ecc1-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\>Get-AzureSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="4ecc1-110">這個命令會傳回展開屬性的資料庫，其中包含服務層顧問資訊。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

## <span data-ttu-id="4ecc1-111">參數</span><span class="sxs-lookup"><span data-stu-id="4ecc1-111">PARAMETERS</span></span>

### <span data-ttu-id="4ecc1-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4ecc1-112">-DatabaseName</span></span>
<span data-ttu-id="4ecc1-113">指定要取得之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-113">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="4ecc1-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ecc1-114">-ResourceGroupName</span></span>
<span data-ttu-id="4ecc1-115">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-115">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4ecc1-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4ecc1-116">-ServerName</span></span>
<span data-ttu-id="4ecc1-117">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4ecc1-118">-確認</span><span class="sxs-lookup"><span data-stu-id="4ecc1-118">-Confirm</span></span>
<span data-ttu-id="4ecc1-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ecc1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ecc1-120">-WhatIf</span></span>
<span data-ttu-id="4ecc1-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ecc1-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ecc1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecc1-123">-DefaultProfile</span></span>
<span data-ttu-id="4ecc1-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ecc1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecc1-125">CommonParameters</span></span>
<span data-ttu-id="4ecc1-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecc1-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ecc1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecc1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="4ecc1-128">INPUTS</span></span>

## <span data-ttu-id="4ecc1-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4ecc1-129">OUTPUTS</span></span>

## <span data-ttu-id="4ecc1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4ecc1-130">NOTES</span></span>

## <span data-ttu-id="4ecc1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ecc1-131">RELATED LINKS</span></span>

[<span data-ttu-id="4ecc1-132">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="4ecc1-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
