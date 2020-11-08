---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: f408edfa0bcdff88fe7577a7cdb6549dcd722dc2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796974"
---
# <span data-ttu-id="72be3-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="72be3-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="72be3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72be3-102">SYNOPSIS</span></span>
<span data-ttu-id="72be3-103">修改 SQL 資料庫伺服器的屬性。</span><span class="sxs-lookup"><span data-stu-id="72be3-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="72be3-104">句法</span><span class="sxs-lookup"><span data-stu-id="72be3-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-MinimalTlsVersion <String>] [-PublicNetworkAccess <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72be3-105">說明</span><span class="sxs-lookup"><span data-stu-id="72be3-105">DESCRIPTION</span></span>
<span data-ttu-id="72be3-106">**AzSqlServer** Cmdlet 會修改 Azure SQL 資料庫伺服器的屬性。</span><span class="sxs-lookup"><span data-stu-id="72be3-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="72be3-107">示例</span><span class="sxs-lookup"><span data-stu-id="72be3-107">EXAMPLES</span></span>

### <span data-ttu-id="72be3-108">範例1：重設系統管理員密碼</span><span class="sxs-lookup"><span data-stu-id="72be3-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="72be3-109">這個命令會在名為 server01 的 AzureSQL 伺服器上重設系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="72be3-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="72be3-110">參數</span><span class="sxs-lookup"><span data-stu-id="72be3-110">PARAMETERS</span></span>

### <span data-ttu-id="72be3-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="72be3-111">-AssignIdentity</span></span>
<span data-ttu-id="72be3-112">針對此伺服器產生並指派 Azure Active Directory 身分識別，以搭配諸如 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="72be3-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="72be3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72be3-113">-DefaultProfile</span></span>
<span data-ttu-id="72be3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="72be3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72be3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="72be3-115">-Force</span></span>
<span data-ttu-id="72be3-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="72be3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72be3-117">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="72be3-117">-PublicNetworkAccess</span></span>
<span data-ttu-id="72be3-118">接受標誌、啟用/停用，以指定是否允許公用網路存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="72be3-118">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="72be3-119">停用時，只有透過私人連結建立的連線才能到達此伺服器。</span><span class="sxs-lookup"><span data-stu-id="72be3-119">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72be3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72be3-120">-ResourceGroupName</span></span>
<span data-ttu-id="72be3-121">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="72be3-121">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="72be3-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72be3-122">-ServerName</span></span>
<span data-ttu-id="72be3-123">指定此 Cmdlet 修改的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="72be3-123">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72be3-124">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="72be3-124">-ServerVersion</span></span>
<span data-ttu-id="72be3-125">指定此 Cmdlet 變更伺服器的版本。</span><span class="sxs-lookup"><span data-stu-id="72be3-125">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="72be3-126">此參數可接受的值為：2.0 和12.0。</span><span class="sxs-lookup"><span data-stu-id="72be3-126">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="72be3-127">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="72be3-127">-SqlAdministratorPassword</span></span>
<span data-ttu-id="72be3-128">針對資料庫伺服器管理員，指定新的密碼（作為 **SecureString** ）。</span><span class="sxs-lookup"><span data-stu-id="72be3-128">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="72be3-129">若要取得 **SecureString** ，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72be3-129">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="72be3-130">如需詳細資訊，請輸入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="72be3-130">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72be3-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="72be3-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="72be3-132">要針對 Sql Server 強制執行的最小 TLS 版本</span><span class="sxs-lookup"><span data-stu-id="72be3-132">The minimal TLS version to enforce for Sql Server</span></span>

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

### <span data-ttu-id="72be3-133">-標記</span><span class="sxs-lookup"><span data-stu-id="72be3-133">-Tags</span></span>
<span data-ttu-id="72be3-134">指定此 Cmdlet 與伺服器關聯的標記字典。</span><span class="sxs-lookup"><span data-stu-id="72be3-134">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="72be3-135">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="72be3-135">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="72be3-136">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="72be3-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="72be3-137">-確認</span><span class="sxs-lookup"><span data-stu-id="72be3-137">-Confirm</span></span>
<span data-ttu-id="72be3-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="72be3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72be3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72be3-139">-WhatIf</span></span>
<span data-ttu-id="72be3-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72be3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72be3-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72be3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72be3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72be3-142">CommonParameters</span></span>
<span data-ttu-id="72be3-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72be3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72be3-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="72be3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72be3-145">輸入</span><span class="sxs-lookup"><span data-stu-id="72be3-145">INPUTS</span></span>

### <span data-ttu-id="72be3-146">System.object</span><span class="sxs-lookup"><span data-stu-id="72be3-146">System.String</span></span>

## <span data-ttu-id="72be3-147">輸出</span><span class="sxs-lookup"><span data-stu-id="72be3-147">OUTPUTS</span></span>

### <span data-ttu-id="72be3-148">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="72be3-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="72be3-149">筆記</span><span class="sxs-lookup"><span data-stu-id="72be3-149">NOTES</span></span>

## <span data-ttu-id="72be3-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="72be3-150">RELATED LINKS</span></span>

[<span data-ttu-id="72be3-151">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="72be3-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)