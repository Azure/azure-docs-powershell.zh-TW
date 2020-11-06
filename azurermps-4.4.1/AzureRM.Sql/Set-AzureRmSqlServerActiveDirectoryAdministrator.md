---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 76d5c2fc90b4e0e518aa022a97c6b9ce369715db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450779"
---
# <span data-ttu-id="b8d43-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b8d43-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="b8d43-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8d43-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d43-103">為 SQL Server 置備 Azure AD 管理員。</span><span class="sxs-lookup"><span data-stu-id="b8d43-103">Provisions an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8d43-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8d43-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8d43-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8d43-105">DESCRIPTION</span></span>
<span data-ttu-id="b8d43-106">AzureRmSqlServerActiveDirectoryAdministrator Cmdlet 會在目前的訂閱中，為 AzureSQL Server (Azure AD) 管理員 **設定** Azure Active Directory。</span><span class="sxs-lookup"><span data-stu-id="b8d43-106">The **Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

<span data-ttu-id="b8d43-107">您一次只能提供一個系統管理員。</span><span class="sxs-lookup"><span data-stu-id="b8d43-107">You can provision only one administrator at a time.</span></span>

<span data-ttu-id="b8d43-108">下列 Azure AD 的成員可設為 SQL Server 系統管理員：</span><span class="sxs-lookup"><span data-stu-id="b8d43-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>

- <span data-ttu-id="b8d43-109">Azure AD 的原生成員</span><span class="sxs-lookup"><span data-stu-id="b8d43-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="b8d43-110">Azure AD 的聯合成員</span><span class="sxs-lookup"><span data-stu-id="b8d43-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="b8d43-111">從其他屬於原生或同盟成員的 Azure 廣告匯入的成員</span><span class="sxs-lookup"><span data-stu-id="b8d43-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="b8d43-112">已建立為安全性群組的 Azure AD 群組</span><span class="sxs-lookup"><span data-stu-id="b8d43-112">Azure AD groups created as security groups</span></span>

<span data-ttu-id="b8d43-113">Microsoft 帳戶（例如 Outlook.com、Hotmail.com 或 Live.com 網域中的帳戶）不受系統管理員支援。</span><span class="sxs-lookup"><span data-stu-id="b8d43-113">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="b8d43-114">其他來賓帳戶（例如 Gmail.com 或 Yahoo.com 網域中的帳戶）不受系統管理員支援。</span><span class="sxs-lookup"><span data-stu-id="b8d43-114">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>

<span data-ttu-id="b8d43-115">我們建議您以系統管理員身分提供專用的 Azure AD 群組。</span><span class="sxs-lookup"><span data-stu-id="b8d43-115">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="b8d43-116">示例</span><span class="sxs-lookup"><span data-stu-id="b8d43-116">EXAMPLES</span></span>

### <span data-ttu-id="b8d43-117">範例1：為伺服器提供管理員群組</span><span class="sxs-lookup"><span data-stu-id="b8d43-117">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="b8d43-118">這個命令會為名為 Server01 的伺服器提供一個名為 Dba 的 Azure AD 管理員群組。</span><span class="sxs-lookup"><span data-stu-id="b8d43-118">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="b8d43-119">此伺服器與資源群組 ResourceGroup01 相關聯。</span><span class="sxs-lookup"><span data-stu-id="b8d43-119">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="b8d43-120">範例2：為伺服器提供管理員使用者</span><span class="sxs-lookup"><span data-stu-id="b8d43-120">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="b8d43-121">這個命令會將 Azure AD 使用者設為名為 Server01 的伺服器的管理員。</span><span class="sxs-lookup"><span data-stu-id="b8d43-121">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="b8d43-122">範例3：透過指定管理員群組的識別碼來提供該群組</span><span class="sxs-lookup"><span data-stu-id="b8d43-122">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="b8d43-123">這個命令會為名為 Server01 的伺服器提供一個名為 Dba 的 Azure AD 管理員群組。</span><span class="sxs-lookup"><span data-stu-id="b8d43-123">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="b8d43-124">命令會指定 *ObjectId* 參數的 ID。</span><span class="sxs-lookup"><span data-stu-id="b8d43-124">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="b8d43-125">這可確保即使群組的顯示名稱不是唯一的，命令也會成功。</span><span class="sxs-lookup"><span data-stu-id="b8d43-125">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="b8d43-126">參數</span><span class="sxs-lookup"><span data-stu-id="b8d43-126">PARAMETERS</span></span>

### <span data-ttu-id="b8d43-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b8d43-127">-DisplayName</span></span>
<span data-ttu-id="b8d43-128">指定此 Cmdlet 所配之 Azure AD 管理員的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b8d43-128">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="b8d43-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b8d43-129">-ObjectId</span></span>
<span data-ttu-id="b8d43-130">指定此 Cmdlet 所配之 Azure AD 管理員的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8d43-130">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="b8d43-131">如果顯示名稱不是唯一的，您必須指定此參數的值。</span><span class="sxs-lookup"><span data-stu-id="b8d43-131">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="b8d43-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d43-132">-ResourceGroupName</span></span>
<span data-ttu-id="b8d43-133">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8d43-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b8d43-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b8d43-134">-ServerName</span></span>
<span data-ttu-id="b8d43-135">指定此 Cmdlet 為其提供管理員的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b8d43-135">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="b8d43-136">-確認</span><span class="sxs-lookup"><span data-stu-id="b8d43-136">-Confirm</span></span>
<span data-ttu-id="b8d43-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8d43-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8d43-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8d43-138">-WhatIf</span></span>
<span data-ttu-id="b8d43-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8d43-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8d43-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8d43-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8d43-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d43-141">-DefaultProfile</span></span>
<span data-ttu-id="b8d43-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8d43-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8d43-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d43-143">CommonParameters</span></span>
<span data-ttu-id="b8d43-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8d43-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d43-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8d43-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d43-146">輸入</span><span class="sxs-lookup"><span data-stu-id="b8d43-146">INPUTS</span></span>

## <span data-ttu-id="b8d43-147">輸出</span><span class="sxs-lookup"><span data-stu-id="b8d43-147">OUTPUTS</span></span>

### <span data-ttu-id="b8d43-148">AzureSqlServerActiveDirectoryAdministratorModel 中的 [ServerActiveDirectoryAdministrator]</span><span class="sxs-lookup"><span data-stu-id="b8d43-148">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="b8d43-149">筆記</span><span class="sxs-lookup"><span data-stu-id="b8d43-149">NOTES</span></span>

## <span data-ttu-id="b8d43-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8d43-150">RELATED LINKS</span></span>

[<span data-ttu-id="b8d43-151">AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b8d43-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="b8d43-152">移除-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b8d43-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="b8d43-153">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b8d43-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


