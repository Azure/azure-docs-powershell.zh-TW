---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 09b7ebf1f88479bca847566b2da93feb83b18571
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907477"
---
# <span data-ttu-id="09dbf-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="09dbf-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="09dbf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="09dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="09dbf-103">獲得 SQL Server 的 Azure AD 系統管理員相關資訊。</span><span class="sxs-lookup"><span data-stu-id="09dbf-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="09dbf-104">語法</span><span class="sxs-lookup"><span data-stu-id="09dbf-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09dbf-105">描述</span><span class="sxs-lookup"><span data-stu-id="09dbf-105">DESCRIPTION</span></span>
<span data-ttu-id="09dbf-106">**Get-AzSqlServerActiveDirectoryAdministrator** Cmdlet 會取得目前訂閱中 Azure Active Directory (Azure AD) 系統管理員的資訊。</span><span class="sxs-lookup"><span data-stu-id="09dbf-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="09dbf-107">例子</span><span class="sxs-lookup"><span data-stu-id="09dbf-107">EXAMPLES</span></span>

### <span data-ttu-id="09dbf-108">範例 1：瞭解伺服器系統管理員的資訊</span><span class="sxs-lookup"><span data-stu-id="09dbf-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="09dbf-109">此命令會針對與 ResourceGroup01 資源群組相關聯的伺服器伺服器，獲得 Azure AD 系統管理員的資訊。</span><span class="sxs-lookup"><span data-stu-id="09dbf-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="09dbf-110">參數</span><span class="sxs-lookup"><span data-stu-id="09dbf-110">PARAMETERS</span></span>

### <span data-ttu-id="09dbf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09dbf-111">-DefaultProfile</span></span>
<span data-ttu-id="09dbf-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="09dbf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09dbf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09dbf-113">-ResourceGroupName</span></span>
<span data-ttu-id="09dbf-114">指定指派給 SQL Server 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="09dbf-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="09dbf-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="09dbf-115">-ServerName</span></span>
<span data-ttu-id="09dbf-116">指定此 Cmdlet 會獲得資訊的 SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="09dbf-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="09dbf-117">-確認</span><span class="sxs-lookup"><span data-stu-id="09dbf-117">-Confirm</span></span>
<span data-ttu-id="09dbf-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="09dbf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09dbf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09dbf-119">-WhatIf</span></span>
<span data-ttu-id="09dbf-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09dbf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09dbf-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09dbf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09dbf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09dbf-122">CommonParameters</span></span>
<span data-ttu-id="09dbf-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="09dbf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09dbf-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09dbf-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09dbf-125">輸入</span><span class="sxs-lookup"><span data-stu-id="09dbf-125">INPUTS</span></span>

### <span data-ttu-id="09dbf-126">System.String</span><span class="sxs-lookup"><span data-stu-id="09dbf-126">System.String</span></span>

## <span data-ttu-id="09dbf-127">輸出</span><span class="sxs-lookup"><span data-stu-id="09dbf-127">OUTPUTS</span></span>

### <span data-ttu-id="09dbf-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="09dbf-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="09dbf-129">筆記</span><span class="sxs-lookup"><span data-stu-id="09dbf-129">NOTES</span></span>

## <span data-ttu-id="09dbf-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="09dbf-130">RELATED LINKS</span></span>

[<span data-ttu-id="09dbf-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="09dbf-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="09dbf-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="09dbf-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="09dbf-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="09dbf-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="09dbf-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="09dbf-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


