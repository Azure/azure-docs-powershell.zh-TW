---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967014"
---
# <span data-ttu-id="93f4e-101">Get-AzureSqlDatabaseServiceObjective</span><span class="sxs-lookup"><span data-stu-id="93f4e-101">Get-AzureSqlDatabaseServiceObjective</span></span>

## <span data-ttu-id="93f4e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="93f4e-103">取得 Azure SQL 資料庫伺服器的服務目標。</span><span class="sxs-lookup"><span data-stu-id="93f4e-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="93f4e-104">句法</span><span class="sxs-lookup"><span data-stu-id="93f4e-104">SYNTAX</span></span>

### <span data-ttu-id="93f4e-105">ByConnectionCoNtext (預設) </span><span class="sxs-lookup"><span data-stu-id="93f4e-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="93f4e-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="93f4e-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="93f4e-107">說明</span><span class="sxs-lookup"><span data-stu-id="93f4e-107">DESCRIPTION</span></span>
<span data-ttu-id="93f4e-108">**AzureSqlDatabaseServiceObjective** Cmdlet 會取得 Azure SQL 資料庫伺服器的服務目標。</span><span class="sxs-lookup"><span data-stu-id="93f4e-108">The **Get-AzureSqlDatabaseServiceObjective** cmdlet gets service objectives for an Azure SQL Database server.</span></span>
<span data-ttu-id="93f4e-109">服務目標稱為效能等級。</span><span class="sxs-lookup"><span data-stu-id="93f4e-109">Service objectives are referred to as performance levels.</span></span>
<span data-ttu-id="93f4e-110">如果您沒有指定服務目標，這個 Cmdlet 會傳回指定伺服器的所有有效服務目標。</span><span class="sxs-lookup"><span data-stu-id="93f4e-110">If you do not specify a service objective, this cmdlet returns all valid service objectives for the specified server.</span></span>

<span data-ttu-id="93f4e-111">這個 Cmdlet 適用于基本、標準和 Premium 服務層級。</span><span class="sxs-lookup"><span data-stu-id="93f4e-111">This cmdlet applies to Basic, Standard, and Premium service tiers.</span></span>

## <span data-ttu-id="93f4e-112">示例</span><span class="sxs-lookup"><span data-stu-id="93f4e-112">EXAMPLES</span></span>

### <span data-ttu-id="93f4e-113">範例1：使用連接內容取得所有服務目標</span><span class="sxs-lookup"><span data-stu-id="93f4e-113">Example 1: Get all the service objectives by using a connection context</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

<span data-ttu-id="93f4e-114">這個命令會取得連接內容 $CoNtext 所指定之伺服器的所有服務目標。</span><span class="sxs-lookup"><span data-stu-id="93f4e-114">This command gets all the service objectives for the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="93f4e-115">範例2：使用伺服器名稱取得所有服務目標</span><span class="sxs-lookup"><span data-stu-id="93f4e-115">Example 2: Get all the service objectives by using a server name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

<span data-ttu-id="93f4e-116">這個命令會取得伺服器名為 Server01 的所有服務目標。</span><span class="sxs-lookup"><span data-stu-id="93f4e-116">This command gets all the service objectives for the server named Server01.</span></span>

## <span data-ttu-id="93f4e-117">參數</span><span class="sxs-lookup"><span data-stu-id="93f4e-117">PARAMETERS</span></span>

### <span data-ttu-id="93f4e-118">-內容</span><span class="sxs-lookup"><span data-stu-id="93f4e-118">-Context</span></span>
<span data-ttu-id="93f4e-119">指定伺服器的連接內容。</span><span class="sxs-lookup"><span data-stu-id="93f4e-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93f4e-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="93f4e-120">-Profile</span></span>
<span data-ttu-id="93f4e-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="93f4e-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93f4e-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="93f4e-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f4e-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="93f4e-123">-ServerName</span></span>
<span data-ttu-id="93f4e-124">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="93f4e-124">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93f4e-125">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="93f4e-125">-ServiceObjective</span></span>
<span data-ttu-id="93f4e-126">指定代表此 Cmdlet 所取得之服務目標的物件。</span><span class="sxs-lookup"><span data-stu-id="93f4e-126">Specifies an object that represents the service objective that this cmdlet gets.</span></span>
<span data-ttu-id="93f4e-127">有效值為：</span><span class="sxs-lookup"><span data-stu-id="93f4e-127">Valid values are:</span></span> 

- <span data-ttu-id="93f4e-128">基本： dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="93f4e-128">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="93f4e-129">標準 (S0) ： f1173c43-91bd-4aaa-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="93f4e-129">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="93f4e-130">標準 (S1) ：1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="93f4e-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="93f4e-131">標準 (S2) ：455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="93f4e-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="93f4e-132">\* 標準 (S3) ：789681b8-ca10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="93f4e-132">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="93f4e-133">Premium (P1) ：7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="93f4e-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="93f4e-134">Premium (P1) ：7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="93f4e-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="93f4e-135">Premium (P2) ： a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="93f4e-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="93f4e-136">Premium (P3) ： a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="93f4e-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="93f4e-137">\* 標準 (S3) 是最新的 SQL 資料庫更新 V12 (preview) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="93f4e-137">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="93f4e-138">如需詳細資訊，請參閱 azure [SQL 資料庫 V12 Preview 中的新功能](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) (`https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` azure library 中的) 。</span><span class="sxs-lookup"><span data-stu-id="93f4e-138">For more information, see [What's New in the Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) (`https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/`) in the Azure library.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93f4e-139">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="93f4e-139">-ServiceObjectiveName</span></span>
<span data-ttu-id="93f4e-140">指定要取得之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="93f4e-140">Specifies the name of a service objective to get.</span></span>
<span data-ttu-id="93f4e-141">有效值為： Basic、S0、S1、S2、S3、P1、P2 及 P3。</span><span class="sxs-lookup"><span data-stu-id="93f4e-141">Valid values are: Basic, S0, S1, S2, S3, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="93f4e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f4e-142">CommonParameters</span></span>
<span data-ttu-id="93f4e-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93f4e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f4e-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93f4e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f4e-145">輸入</span><span class="sxs-lookup"><span data-stu-id="93f4e-145">INPUTS</span></span>

### <span data-ttu-id="93f4e-146">SqlDatabase. ServiceObjective （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="93f4e-146">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective</span></span>

## <span data-ttu-id="93f4e-147">輸出</span><span class="sxs-lookup"><span data-stu-id="93f4e-147">OUTPUTS</span></span>

### <span data-ttu-id="93f4e-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span><span class="sxs-lookup"><span data-stu-id="93f4e-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span></span>

## <span data-ttu-id="93f4e-149">筆記</span><span class="sxs-lookup"><span data-stu-id="93f4e-149">NOTES</span></span>

## <span data-ttu-id="93f4e-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="93f4e-150">RELATED LINKS</span></span>

[<span data-ttu-id="93f4e-151">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="93f4e-151">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="93f4e-152">取得服務層級目標</span><span class="sxs-lookup"><span data-stu-id="93f4e-152">Get Service Level Objective</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[<span data-ttu-id="93f4e-153">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="93f4e-153">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="93f4e-154">新-AzureSqlDatabaseServerCoNtext</span><span class="sxs-lookup"><span data-stu-id="93f4e-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


