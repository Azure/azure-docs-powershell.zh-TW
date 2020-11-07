---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: b8f7d04a709ebb14ed6a7a76cffab556c13d26ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626207"
---
# <span data-ttu-id="ffe3c-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="ffe3c-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="ffe3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ffe3c-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe3c-103">取得資料庫地域備份原則。</span><span class="sxs-lookup"><span data-stu-id="ffe3c-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffe3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ffe3c-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffe3c-105">說明</span><span class="sxs-lookup"><span data-stu-id="ffe3c-105">DESCRIPTION</span></span>
<span data-ttu-id="ffe3c-106">**AzureRmSqlDatabaseGeoBackupPolicy** Cmdlet 會取得已登錄至此資料庫的 geo 備份原則。</span><span class="sxs-lookup"><span data-stu-id="ffe3c-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="ffe3c-107">這是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="ffe3c-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="ffe3c-108">示例</span><span class="sxs-lookup"><span data-stu-id="ffe3c-108">EXAMPLES</span></span>

## <span data-ttu-id="ffe3c-109">參數</span><span class="sxs-lookup"><span data-stu-id="ffe3c-109">PARAMETERS</span></span>

### <span data-ttu-id="ffe3c-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ffe3c-110">-DatabaseName</span></span>
<span data-ttu-id="ffe3c-111">指定此 Cmdlet 取得 geo 備份原則之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffe3c-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="ffe3c-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffe3c-112">-ResourceGroupName</span></span>
<span data-ttu-id="ffe3c-113">指定包含此資料庫之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffe3c-113">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="ffe3c-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ffe3c-114">-ServerName</span></span>
<span data-ttu-id="ffe3c-115">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ffe3c-115">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ffe3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe3c-116">-DefaultProfile</span></span>
<span data-ttu-id="ffe3c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ffe3c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffe3c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe3c-118">CommonParameters</span></span>
<span data-ttu-id="ffe3c-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ffe3c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe3c-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ffe3c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe3c-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ffe3c-121">INPUTS</span></span>

## <span data-ttu-id="ffe3c-122">輸出</span><span class="sxs-lookup"><span data-stu-id="ffe3c-122">OUTPUTS</span></span>

## <span data-ttu-id="ffe3c-123">筆記</span><span class="sxs-lookup"><span data-stu-id="ffe3c-123">NOTES</span></span>

## <span data-ttu-id="ffe3c-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffe3c-124">RELATED LINKS</span></span>

[<span data-ttu-id="ffe3c-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="ffe3c-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="ffe3c-126">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ffe3c-126">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
