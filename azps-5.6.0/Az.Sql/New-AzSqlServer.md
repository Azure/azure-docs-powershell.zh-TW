---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: 182dfddf4acc294b2afb994b13db4f1644d95aab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908337"
---
# <span data-ttu-id="bfeef-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="bfeef-101">New-AzSqlServer</span></span>

## <span data-ttu-id="bfeef-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bfeef-102">SYNOPSIS</span></span>
<span data-ttu-id="bfeef-103">建立 SQL Database 伺服器。</span><span class="sxs-lookup"><span data-stu-id="bfeef-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="bfeef-104">語法</span><span class="sxs-lookup"><span data-stu-id="bfeef-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfeef-105">描述</span><span class="sxs-lookup"><span data-stu-id="bfeef-105">DESCRIPTION</span></span>
<span data-ttu-id="bfeef-106">**New-AzSqlServer** Cmdlet 會建立 Azure SQL Database 伺服器。</span><span class="sxs-lookup"><span data-stu-id="bfeef-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="bfeef-107">例子</span><span class="sxs-lookup"><span data-stu-id="bfeef-107">EXAMPLES</span></span>

### <span data-ttu-id="bfeef-108">範例 1：建立新 Azure SQL Database 伺服器</span><span class="sxs-lookup"><span data-stu-id="bfeef-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="bfeef-109">此命令會建立版本 12 Azure SQL Database 伺服器。</span><span class="sxs-lookup"><span data-stu-id="bfeef-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="bfeef-110">參數</span><span class="sxs-lookup"><span data-stu-id="bfeef-110">PARAMETERS</span></span>

### <span data-ttu-id="bfeef-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfeef-111">-AsJob</span></span>
<span data-ttu-id="bfeef-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bfeef-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bfeef-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="bfeef-113">-AssignIdentity</span></span>
<span data-ttu-id="bfeef-114">為此伺服器產生並指派 Azure Active Directory 身分識別，以用於 Azure KeyVault 等重要管理服務。</span><span class="sxs-lookup"><span data-stu-id="bfeef-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="bfeef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfeef-115">-DefaultProfile</span></span>
<span data-ttu-id="bfeef-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="bfeef-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfeef-117">-位置</span><span class="sxs-lookup"><span data-stu-id="bfeef-117">-Location</span></span>
<span data-ttu-id="bfeef-118">指定此 Cmdlet 建立伺服器的資料中心位置。</span><span class="sxs-lookup"><span data-stu-id="bfeef-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeef-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="bfeef-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="bfeef-120">針對 Sql Server 強制執行的最小 TLS 版本</span><span class="sxs-lookup"><span data-stu-id="bfeef-120">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeef-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="bfeef-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="bfeef-122">使用已啟用/停用的標號來指定是否允許公用網路存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="bfeef-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="bfeef-123">停用時，只有透過私人連結所建立的連結可以連至此伺服器。</span><span class="sxs-lookup"><span data-stu-id="bfeef-123">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfeef-124">-ResourceGroupName</span></span>
<span data-ttu-id="bfeef-125">指定此 Cmdlet 指派伺服器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="bfeef-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="bfeef-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bfeef-126">-ServerName</span></span>
<span data-ttu-id="bfeef-127">指定新伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="bfeef-127">Specifies the name of the new server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeef-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="bfeef-128">-ServerVersion</span></span>
<span data-ttu-id="bfeef-129">指定新伺服器的版本。</span><span class="sxs-lookup"><span data-stu-id="bfeef-129">Specifies the version of the new server.</span></span> <span data-ttu-id="bfeef-130">此參數可接受的值為：2.0 和 12.0。</span><span class="sxs-lookup"><span data-stu-id="bfeef-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="bfeef-131">指定 2.0 以建立版本 11 伺服器，或指定 12.0 以建立版本 12 伺服器。</span><span class="sxs-lookup"><span data-stu-id="bfeef-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeef-132">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="bfeef-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="bfeef-133">指定新伺服器的 SQL Database 伺服器系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="bfeef-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="bfeef-134">若要取得 **PSCredential 物件** ，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bfeef-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="bfeef-135">如需要詳細資訊，請鍵入 `Get-Help
Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="bfeef-135">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeef-136">-標記</span><span class="sxs-lookup"><span data-stu-id="bfeef-136">-Tags</span></span>
<span data-ttu-id="bfeef-137">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="bfeef-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bfeef-138">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="bfeef-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeef-139">-確認</span><span class="sxs-lookup"><span data-stu-id="bfeef-139">-Confirm</span></span>
<span data-ttu-id="bfeef-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bfeef-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfeef-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfeef-141">-WhatIf</span></span>
<span data-ttu-id="bfeef-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bfeef-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfeef-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bfeef-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfeef-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfeef-144">CommonParameters</span></span>
<span data-ttu-id="bfeef-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bfeef-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfeef-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfeef-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfeef-147">輸入</span><span class="sxs-lookup"><span data-stu-id="bfeef-147">INPUTS</span></span>

### <span data-ttu-id="bfeef-148">System.String</span><span class="sxs-lookup"><span data-stu-id="bfeef-148">System.String</span></span>

## <span data-ttu-id="bfeef-149">輸出</span><span class="sxs-lookup"><span data-stu-id="bfeef-149">OUTPUTS</span></span>

### <span data-ttu-id="bfeef-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="bfeef-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="bfeef-151">筆記</span><span class="sxs-lookup"><span data-stu-id="bfeef-151">NOTES</span></span>

## <span data-ttu-id="bfeef-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="bfeef-152">RELATED LINKS</span></span>

[<span data-ttu-id="bfeef-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="bfeef-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="bfeef-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="bfeef-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="bfeef-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="bfeef-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="bfeef-156">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bfeef-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="bfeef-157">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="bfeef-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
