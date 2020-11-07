---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: a754ff33cba0bcf6324be0eb947b592b8fd4a622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624540"
---
# <span data-ttu-id="845b1-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="845b1-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="845b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="845b1-102">SYNOPSIS</span></span>
<span data-ttu-id="845b1-103">建立 SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="845b1-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="845b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="845b1-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="845b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="845b1-105">DESCRIPTION</span></span>
<span data-ttu-id="845b1-106">**新的-AzureRmSqlServer** Cmdlet 會建立 Azure SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="845b1-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="845b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="845b1-107">EXAMPLES</span></span>

### <span data-ttu-id="845b1-108">範例1：建立新的 Azure SQL 資料庫伺服器</span><span class="sxs-lookup"><span data-stu-id="845b1-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="845b1-109">這個命令會建立版本 12 Azure SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="845b1-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="845b1-110">參數</span><span class="sxs-lookup"><span data-stu-id="845b1-110">PARAMETERS</span></span>

### <span data-ttu-id="845b1-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="845b1-111">-AssignIdentity</span></span>
<span data-ttu-id="845b1-112">針對此伺服器產生並指派 Azure Active Directory 身分識別，以搭配諸如 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="845b1-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="845b1-113">-位置</span><span class="sxs-lookup"><span data-stu-id="845b1-113">-Location</span></span>
<span data-ttu-id="845b1-114">指定此 Cmdlet 建立伺服器的資料中心位置。</span><span class="sxs-lookup"><span data-stu-id="845b1-114">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="845b1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="845b1-115">-ResourceGroupName</span></span>
<span data-ttu-id="845b1-116">指定此 Cmdlet 指派伺服器的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="845b1-116">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="845b1-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="845b1-117">-ServerName</span></span>
<span data-ttu-id="845b1-118">指定新伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="845b1-118">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="845b1-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="845b1-119">-ServerVersion</span></span>
<span data-ttu-id="845b1-120">指定新伺服器的版本。</span><span class="sxs-lookup"><span data-stu-id="845b1-120">Specifies the version of the new server.</span></span> <span data-ttu-id="845b1-121">此參數可接受的值為：2.0 和12.0。</span><span class="sxs-lookup"><span data-stu-id="845b1-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="845b1-122">指定2.0 來建立版本11伺服器，或指定12.0 以建立版本12的伺服器。</span><span class="sxs-lookup"><span data-stu-id="845b1-122">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="845b1-123">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="845b1-123">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="845b1-124">指定新伺服器的 SQL 資料庫伺服器管理員認證。</span><span class="sxs-lookup"><span data-stu-id="845b1-124">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="845b1-125">若要取得 **PSCredential** 物件，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="845b1-125">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="845b1-126">如需詳細資訊，請輸入 `Get-Help
Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="845b1-126">For more information, type `Get-Help
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

### <span data-ttu-id="845b1-127">-標記</span><span class="sxs-lookup"><span data-stu-id="845b1-127">-Tags</span></span>
<span data-ttu-id="845b1-128">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="845b1-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="845b1-129">例如：</span><span class="sxs-lookup"><span data-stu-id="845b1-129">For example:</span></span>

<span data-ttu-id="845b1-130">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="845b1-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="845b1-131">-確認</span><span class="sxs-lookup"><span data-stu-id="845b1-131">-Confirm</span></span>
<span data-ttu-id="845b1-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="845b1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="845b1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="845b1-133">-WhatIf</span></span>
<span data-ttu-id="845b1-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="845b1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="845b1-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="845b1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="845b1-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="845b1-136">-DefaultProfile</span></span>
<span data-ttu-id="845b1-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="845b1-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="845b1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="845b1-138">CommonParameters</span></span>
<span data-ttu-id="845b1-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="845b1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="845b1-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="845b1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="845b1-141">輸入</span><span class="sxs-lookup"><span data-stu-id="845b1-141">INPUTS</span></span>

## <span data-ttu-id="845b1-142">輸出</span><span class="sxs-lookup"><span data-stu-id="845b1-142">OUTPUTS</span></span>

### <span data-ttu-id="845b1-143">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="845b1-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="845b1-144">筆記</span><span class="sxs-lookup"><span data-stu-id="845b1-144">NOTES</span></span>

## <span data-ttu-id="845b1-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="845b1-145">RELATED LINKS</span></span>

[<span data-ttu-id="845b1-146">AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="845b1-146">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="845b1-147">移除-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="845b1-147">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="845b1-148">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="845b1-148">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="845b1-149">新-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="845b1-149">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="845b1-150">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="845b1-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
