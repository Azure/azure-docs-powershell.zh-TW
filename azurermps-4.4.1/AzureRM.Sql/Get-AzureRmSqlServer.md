---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: f2d687ce10edf56fc424c03873c733971f70e546
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453243"
---
# <span data-ttu-id="2a3f8-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2a3f8-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="2a3f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a3f8-102">SYNOPSIS</span></span>
<span data-ttu-id="2a3f8-103">傳回 SQL 資料庫伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a3f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a3f8-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a3f8-105">說明</span><span class="sxs-lookup"><span data-stu-id="2a3f8-105">DESCRIPTION</span></span>
<span data-ttu-id="2a3f8-106">**AzureRmSqlServer** Cmdlet 會傳回一或多個 Azure SQL 資料庫伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="2a3f8-107">指定伺服器的名稱，只查看該伺服器的資訊。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="2a3f8-108">示例</span><span class="sxs-lookup"><span data-stu-id="2a3f8-108">EXAMPLES</span></span>

### <span data-ttu-id="2a3f8-109">範例1：取得指派給資源群組的所有 SQL Server 實例</span><span class="sxs-lookup"><span data-stu-id="2a3f8-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLoginSqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="2a3f8-110">這個命令會取得指派給資源群組 ResourceGroup01 的所有 Azure SQL 資料庫伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="2a3f8-111">範例2：取得 Azure SQL 資料庫伺服器的相關資訊</span><span class="sxs-lookup"><span data-stu-id="2a3f8-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="2a3f8-112">這個命令會取得名為 Server01 的 Azure SQL Database 伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="2a3f8-113">範例3：在訂閱中取得 SQL Server 的所有實例</span><span class="sxs-lookup"><span data-stu-id="2a3f8-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="2a3f8-114">這個命令會取得目前訂閱中所有 Azure SQL Database 伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="2a3f8-115">參數</span><span class="sxs-lookup"><span data-stu-id="2a3f8-115">PARAMETERS</span></span>

### <span data-ttu-id="2a3f8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a3f8-116">-ResourceGroupName</span></span>
<span data-ttu-id="2a3f8-117">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-117">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3f8-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2a3f8-118">-ServerName</span></span>
<span data-ttu-id="2a3f8-119">指定此 Cmdlet 取得的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-119">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3f8-120">-確認</span><span class="sxs-lookup"><span data-stu-id="2a3f8-120">-Confirm</span></span>
<span data-ttu-id="2a3f8-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a3f8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a3f8-122">-WhatIf</span></span>
<span data-ttu-id="2a3f8-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a3f8-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a3f8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a3f8-125">-DefaultProfile</span></span>
<span data-ttu-id="2a3f8-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a3f8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a3f8-127">CommonParameters</span></span>
<span data-ttu-id="2a3f8-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a3f8-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a3f8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a3f8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2a3f8-130">INPUTS</span></span>

## <span data-ttu-id="2a3f8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="2a3f8-131">OUTPUTS</span></span>

### <span data-ttu-id="2a3f8-132">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="2a3f8-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="2a3f8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="2a3f8-133">NOTES</span></span>

## <span data-ttu-id="2a3f8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a3f8-134">RELATED LINKS</span></span>

[<span data-ttu-id="2a3f8-135">新-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2a3f8-135">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="2a3f8-136">移除-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2a3f8-136">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="2a3f8-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2a3f8-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="2a3f8-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="2a3f8-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


