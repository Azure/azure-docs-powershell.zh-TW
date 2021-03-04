---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: ac6b421a64658423857c93ff0c782b0ec84b8c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913106"
---
# <span data-ttu-id="a9b67-101">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a9b67-101">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a9b67-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a9b67-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b67-103">移除 SQL Server 的 Azure AD 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="a9b67-103">Removes an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="a9b67-104">語法</span><span class="sxs-lookup"><span data-stu-id="a9b67-104">SYNTAX</span></span>

```
Remove-AzSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9b67-105">描述</span><span class="sxs-lookup"><span data-stu-id="a9b67-105">DESCRIPTION</span></span>
<span data-ttu-id="a9b67-106">**Remove-AzSqlServerActiveDirectoryAdministrator** Cmdlet 會移除目前訂閱中的 Azure Active Directory (Azure AD) 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="a9b67-106">The **Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="a9b67-107">例子</span><span class="sxs-lookup"><span data-stu-id="a9b67-107">EXAMPLES</span></span>

### <span data-ttu-id="a9b67-108">範例 1：移除系統管理員</span><span class="sxs-lookup"><span data-stu-id="a9b67-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a9b67-109">此命令會移除伺服器名稱為 Server01 的 Azure AD 系統管理員，該伺服器與資源群組 ResourceGroup01 相關聯。</span><span class="sxs-lookup"><span data-stu-id="a9b67-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="a9b67-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9b67-110">PARAMETERS</span></span>

### <span data-ttu-id="a9b67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b67-111">-DefaultProfile</span></span>
<span data-ttu-id="a9b67-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a9b67-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9b67-113">-強制</span><span class="sxs-lookup"><span data-stu-id="a9b67-113">-Force</span></span>
<span data-ttu-id="a9b67-114">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a9b67-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b67-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b67-115">-ResourceGroupName</span></span>
<span data-ttu-id="a9b67-116">指定指派給 SQL Server 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a9b67-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="a9b67-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9b67-117">-ServerName</span></span>
<span data-ttu-id="a9b67-118">指定此 Cmdlet 會移除系統管理員的 SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="a9b67-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="a9b67-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a9b67-119">-Confirm</span></span>
<span data-ttu-id="a9b67-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a9b67-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9b67-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9b67-121">-WhatIf</span></span>
<span data-ttu-id="a9b67-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9b67-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9b67-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9b67-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9b67-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b67-124">CommonParameters</span></span>
<span data-ttu-id="a9b67-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a9b67-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b67-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9b67-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b67-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a9b67-127">INPUTS</span></span>

### <span data-ttu-id="a9b67-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a9b67-128">System.String</span></span>

## <span data-ttu-id="a9b67-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a9b67-129">OUTPUTS</span></span>

### <span data-ttu-id="a9b67-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="a9b67-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="a9b67-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a9b67-131">NOTES</span></span>

## <span data-ttu-id="a9b67-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9b67-132">RELATED LINKS</span></span>

[<span data-ttu-id="a9b67-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a9b67-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a9b67-134">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a9b67-134">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a9b67-135">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="a9b67-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


