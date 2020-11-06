---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: e782ef221474ab3a041fddc7628157fd999796d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447627"
---
# <span data-ttu-id="700e5-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="700e5-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="700e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="700e5-102">SYNOPSIS</span></span>
<span data-ttu-id="700e5-103">取得有關 SQL Server Azure AD 管理員的資訊。</span><span class="sxs-lookup"><span data-stu-id="700e5-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="700e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="700e5-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="700e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="700e5-105">DESCRIPTION</span></span>
<span data-ttu-id="700e5-106">**AzureRmSqlServerActiveDirectoryAdministrator** Cmdlet 會取得 Azure Active Directory (azure AD) 管理員（針對目前訂閱中的 AzureSQL 伺服器）的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="700e5-106">The **Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="700e5-107">示例</span><span class="sxs-lookup"><span data-stu-id="700e5-107">EXAMPLES</span></span>

### <span data-ttu-id="700e5-108">範例1：取得伺服器管理員的相關資訊</span><span class="sxs-lookup"><span data-stu-id="700e5-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="700e5-109">這個命令會針對與名為 ResourceGroup01 的資源群組相關聯的伺服器（名為 Server01），取得 Azure AD 系統管理員的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="700e5-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="700e5-110">參數</span><span class="sxs-lookup"><span data-stu-id="700e5-110">PARAMETERS</span></span>

### <span data-ttu-id="700e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="700e5-111">-DefaultProfile</span></span>
<span data-ttu-id="700e5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="700e5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="700e5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="700e5-113">-ResourceGroupName</span></span>
<span data-ttu-id="700e5-114">指定指派 SQL Server 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="700e5-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="700e5-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="700e5-115">-ServerName</span></span>
<span data-ttu-id="700e5-116">指定此 Cmdlet 取得資訊之 SQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="700e5-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="700e5-117">-確認</span><span class="sxs-lookup"><span data-stu-id="700e5-117">-Confirm</span></span>
<span data-ttu-id="700e5-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="700e5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="700e5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="700e5-119">-WhatIf</span></span>
<span data-ttu-id="700e5-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="700e5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="700e5-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="700e5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="700e5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="700e5-122">CommonParameters</span></span>
<span data-ttu-id="700e5-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="700e5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="700e5-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="700e5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="700e5-125">輸入</span><span class="sxs-lookup"><span data-stu-id="700e5-125">INPUTS</span></span>

### <span data-ttu-id="700e5-126">所有</span><span class="sxs-lookup"><span data-stu-id="700e5-126">None</span></span>
<span data-ttu-id="700e5-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="700e5-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="700e5-128">輸出</span><span class="sxs-lookup"><span data-stu-id="700e5-128">OUTPUTS</span></span>

### <span data-ttu-id="700e5-129">AzureSqlServerActiveDirectoryAdministratorModel 中的 [ServerActiveDirectoryAdministrator]</span><span class="sxs-lookup"><span data-stu-id="700e5-129">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="700e5-130">筆記</span><span class="sxs-lookup"><span data-stu-id="700e5-130">NOTES</span></span>

## <span data-ttu-id="700e5-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="700e5-131">RELATED LINKS</span></span>

[<span data-ttu-id="700e5-132">移除-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="700e5-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="700e5-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="700e5-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="700e5-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="700e5-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


