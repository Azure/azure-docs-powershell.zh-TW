---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f3492b0f6eb83f2c4a37a6fa073e7f579208cf62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958418"
---
# <span data-ttu-id="02990-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="02990-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="02990-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02990-102">SYNOPSIS</span></span>
<span data-ttu-id="02990-103">取得有關 SQL Server Azure AD 管理員的資訊。</span><span class="sxs-lookup"><span data-stu-id="02990-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="02990-104">句法</span><span class="sxs-lookup"><span data-stu-id="02990-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02990-105">說明</span><span class="sxs-lookup"><span data-stu-id="02990-105">DESCRIPTION</span></span>
<span data-ttu-id="02990-106">**AzSqlServerActiveDirectoryAdministrator** Cmdlet 會取得 Azure Active Directory (azure AD) 管理員（針對目前訂閱中的 AzureSQL 伺服器）的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="02990-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="02990-107">示例</span><span class="sxs-lookup"><span data-stu-id="02990-107">EXAMPLES</span></span>

### <span data-ttu-id="02990-108">範例1：取得伺服器管理員的相關資訊</span><span class="sxs-lookup"><span data-stu-id="02990-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="02990-109">這個命令會針對與名為 ResourceGroup01 的資源群組相關聯的伺服器（名為 Server01），取得 Azure AD 系統管理員的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="02990-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="02990-110">參數</span><span class="sxs-lookup"><span data-stu-id="02990-110">PARAMETERS</span></span>

### <span data-ttu-id="02990-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02990-111">-DefaultProfile</span></span>
<span data-ttu-id="02990-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="02990-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02990-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02990-113">-ResourceGroupName</span></span>
<span data-ttu-id="02990-114">指定指派 SQL Server 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="02990-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="02990-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="02990-115">-ServerName</span></span>
<span data-ttu-id="02990-116">指定此 Cmdlet 取得資訊之 SQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="02990-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="02990-117">-確認</span><span class="sxs-lookup"><span data-stu-id="02990-117">-Confirm</span></span>
<span data-ttu-id="02990-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="02990-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02990-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02990-119">-WhatIf</span></span>
<span data-ttu-id="02990-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02990-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02990-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02990-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02990-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02990-122">CommonParameters</span></span>
<span data-ttu-id="02990-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02990-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02990-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="02990-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02990-125">輸入</span><span class="sxs-lookup"><span data-stu-id="02990-125">INPUTS</span></span>

### <span data-ttu-id="02990-126">System.object</span><span class="sxs-lookup"><span data-stu-id="02990-126">System.String</span></span>

## <span data-ttu-id="02990-127">輸出</span><span class="sxs-lookup"><span data-stu-id="02990-127">OUTPUTS</span></span>

### <span data-ttu-id="02990-128">AzureSqlServerActiveDirectoryAdministratorModel 中的 [ServerActiveDirectoryAdministrator]</span><span class="sxs-lookup"><span data-stu-id="02990-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="02990-129">筆記</span><span class="sxs-lookup"><span data-stu-id="02990-129">NOTES</span></span>

## <span data-ttu-id="02990-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="02990-130">RELATED LINKS</span></span>

[<span data-ttu-id="02990-131">移除-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="02990-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="02990-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="02990-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="02990-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="02990-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="02990-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="02990-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


