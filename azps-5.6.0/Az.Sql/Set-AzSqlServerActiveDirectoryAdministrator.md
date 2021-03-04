---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 37fe534b13226f81c7639275a3c35f3a54d3543b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909306"
---
# <span data-ttu-id="2735b-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="2735b-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="2735b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2735b-102">SYNOPSIS</span></span>
<span data-ttu-id="2735b-103">為 SQL Server 提供 Azure AD 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="2735b-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="2735b-104">語法</span><span class="sxs-lookup"><span data-stu-id="2735b-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2735b-105">描述</span><span class="sxs-lookup"><span data-stu-id="2735b-105">DESCRIPTION</span></span>
<span data-ttu-id="2735b-106">**Set-AzSqlServerActiveDirectoryAdministrator** Cmdlet 會針對目前訂閱中的 AzureSQL Server 提供 Azure Active Directory (Azure AD) 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="2735b-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="2735b-107">您一次只能配置一位系統管理員。</span><span class="sxs-lookup"><span data-stu-id="2735b-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="2735b-108">下列 Azure AD 成員可以以 SQL Server 系統管理員的名下進行設置：</span><span class="sxs-lookup"><span data-stu-id="2735b-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="2735b-109">Azure AD 的原生成員</span><span class="sxs-lookup"><span data-stu-id="2735b-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="2735b-110">Azure AD 的聯盟成員</span><span class="sxs-lookup"><span data-stu-id="2735b-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="2735b-111">從原生或聯盟成員的其他 Azure AD 中匯出成員</span><span class="sxs-lookup"><span data-stu-id="2735b-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="2735b-112">系統管理員不支援以安全性群組方式建立 Azure AD 群組的 Microsoft 帳戶，例如 Outlook.com、Hotmail.com 或 Live.com 網域中的帳戶。</span><span class="sxs-lookup"><span data-stu-id="2735b-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="2735b-113">系統管理員不支援其他來賓帳戶，例如 Gmail.com或Yahoo.com中的來賓帳戶。</span><span class="sxs-lookup"><span data-stu-id="2735b-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="2735b-114">建議您以系統管理員的名將專用 Azure AD 群組進行設置。</span><span class="sxs-lookup"><span data-stu-id="2735b-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="2735b-115">例子</span><span class="sxs-lookup"><span data-stu-id="2735b-115">EXAMPLES</span></span>

### <span data-ttu-id="2735b-116">範例 1：為伺服器提供系統管理員群組</span><span class="sxs-lookup"><span data-stu-id="2735b-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="2735b-117">此命令會為名為 Server01 的伺服器提供名為 DBAs 的 Azure AD 系統管理員群組。</span><span class="sxs-lookup"><span data-stu-id="2735b-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="2735b-118">此伺服器與資源群組 ResourceGroup01 相關聯。</span><span class="sxs-lookup"><span data-stu-id="2735b-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="2735b-119">範例 2：為伺服器提供系統管理員使用者</span><span class="sxs-lookup"><span data-stu-id="2735b-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="2735b-120">此命令會為名為 Server01 的伺服器提供 Azure AD 使用者的系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="2735b-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="2735b-121">範例 3：指定管理員群組的識別碼來提供</span><span class="sxs-lookup"><span data-stu-id="2735b-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="2735b-122">此命令會為名為 Server01 的伺服器提供名為 DBAs 的 Azure AD 系統管理員群組。</span><span class="sxs-lookup"><span data-stu-id="2735b-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="2735b-123">命令會指定 ObjectId 參數 *的識別碼* 。</span><span class="sxs-lookup"><span data-stu-id="2735b-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="2735b-124">這樣即使群組的顯示名稱並非唯一，也能夠確保命令成功。</span><span class="sxs-lookup"><span data-stu-id="2735b-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="2735b-125">參數</span><span class="sxs-lookup"><span data-stu-id="2735b-125">PARAMETERS</span></span>

### <span data-ttu-id="2735b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2735b-126">-DefaultProfile</span></span>
<span data-ttu-id="2735b-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2735b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2735b-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2735b-128">-DisplayName</span></span>
<span data-ttu-id="2735b-129">指定此 Cmdlet 所提供之 Azure AD 系統管理員的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2735b-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="2735b-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2735b-130">-ObjectId</span></span>
<span data-ttu-id="2735b-131">指定此 Cmdlet 所提供之 Azure AD 系統管理員的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="2735b-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="2735b-132">如果顯示名稱並非唯一，您必須為此參數指定值。</span><span class="sxs-lookup"><span data-stu-id="2735b-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2735b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2735b-133">-ResourceGroupName</span></span>
<span data-ttu-id="2735b-134">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="2735b-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2735b-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2735b-135">-ServerName</span></span>
<span data-ttu-id="2735b-136">指定此 Cmdlet 提供系統管理員的 SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="2735b-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="2735b-137">-確認</span><span class="sxs-lookup"><span data-stu-id="2735b-137">-Confirm</span></span>
<span data-ttu-id="2735b-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2735b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2735b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2735b-139">-WhatIf</span></span>
<span data-ttu-id="2735b-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2735b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2735b-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2735b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2735b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2735b-142">CommonParameters</span></span>
<span data-ttu-id="2735b-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2735b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2735b-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2735b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2735b-145">輸入</span><span class="sxs-lookup"><span data-stu-id="2735b-145">INPUTS</span></span>

### <span data-ttu-id="2735b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2735b-146">System.String</span></span>

### <span data-ttu-id="2735b-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="2735b-147">System.Guid</span></span>

## <span data-ttu-id="2735b-148">輸出</span><span class="sxs-lookup"><span data-stu-id="2735b-148">OUTPUTS</span></span>

### <span data-ttu-id="2735b-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="2735b-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="2735b-150">筆記</span><span class="sxs-lookup"><span data-stu-id="2735b-150">NOTES</span></span>

## <span data-ttu-id="2735b-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="2735b-151">RELATED LINKS</span></span>

[<span data-ttu-id="2735b-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="2735b-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="2735b-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="2735b-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="2735b-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="2735b-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="2735b-155">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="2735b-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


