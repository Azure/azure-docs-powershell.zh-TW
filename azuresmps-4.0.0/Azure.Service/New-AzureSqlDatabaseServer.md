---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A0C674FC-A1D8-4068-8CAB-2EE0AECB8E68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 069b96809c0659028135e8c9a28e7e3c0ab8b3ae
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967417"
---
# <span data-ttu-id="82a99-101">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="82a99-101">New-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="82a99-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82a99-102">SYNOPSIS</span></span>
<span data-ttu-id="82a99-103">建立 Azure SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="82a99-103">Creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="82a99-104">句法</span><span class="sxs-lookup"><span data-stu-id="82a99-104">SYNTAX</span></span>

```
New-AzureSqlDatabaseServer -AdministratorLogin <String> -AdministratorLoginPassword <String> -Location <String>
 [-Version <Single>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82a99-105">說明</span><span class="sxs-lookup"><span data-stu-id="82a99-105">DESCRIPTION</span></span>
<span data-ttu-id="82a99-106">**新的 AzureSqlDatabaseServer** Cmdlet 會在目前的訂閱中建立 Azure SQL Database Server 的實例。</span><span class="sxs-lookup"><span data-stu-id="82a99-106">The **New-AzureSqlDatabaseServer** cmdlet creates an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="82a99-107">示例</span><span class="sxs-lookup"><span data-stu-id="82a99-107">EXAMPLES</span></span>

### <span data-ttu-id="82a99-108">範例1：建立伺服器</span><span class="sxs-lookup"><span data-stu-id="82a99-108">Example 1: Create a server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword"
```

<span data-ttu-id="82a99-109">這個命令會建立版本 11 Azure SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="82a99-109">This command creates a version 11 Azure SQL Database server.</span></span>

### <span data-ttu-id="82a99-110">範例2：建立版本12伺服器</span><span class="sxs-lookup"><span data-stu-id="82a99-110">Example 2: Create a version 12 server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword" -Version "12.0"
```

<span data-ttu-id="82a99-111">這個命令會建立版本12伺服器。</span><span class="sxs-lookup"><span data-stu-id="82a99-111">This command creates a version 12 server.</span></span>

## <span data-ttu-id="82a99-112">參數</span><span class="sxs-lookup"><span data-stu-id="82a99-112">PARAMETERS</span></span>

### <span data-ttu-id="82a99-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="82a99-113">-AdministratorLogin</span></span>
<span data-ttu-id="82a99-114">指定新 Azure SQL 資料庫伺服器的系統管理員帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="82a99-114">Specifies the administrator account name for the new Azure SQL Database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a99-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="82a99-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="82a99-116">指定 Azure SQL 資料庫伺服器的系統管理員帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="82a99-116">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="82a99-117">您必須指定強式密碼。</span><span class="sxs-lookup"><span data-stu-id="82a99-117">You must specify a strong password.</span></span>
<span data-ttu-id="82a99-118">如需詳細資訊， [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152)請參閱 https://go.microsoft.com/fwlink/p/?LinkId=154152) 在 Microsoft 開發人員網路上 (強式密碼。</span><span class="sxs-lookup"><span data-stu-id="82a99-118">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a99-119">-Force</span><span class="sxs-lookup"><span data-stu-id="82a99-119">-Force</span></span>
<span data-ttu-id="82a99-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="82a99-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a99-121">-位置</span><span class="sxs-lookup"><span data-stu-id="82a99-121">-Location</span></span>
<span data-ttu-id="82a99-122">指定此 Cmdlet 建立伺服器的資料中心位置。</span><span class="sxs-lookup"><span data-stu-id="82a99-122">Specifies the location of the data center where this cmdlet creates the server.</span></span>
<span data-ttu-id="82a99-123">如需詳細資訊，請參閱 Azure 文件庫中的 [ [Azure 地區](https://azure.microsoft.com/regions/) ] (https://azure.microsoft.com/regions/#services) 。</span><span class="sxs-lookup"><span data-stu-id="82a99-123">For more information, see [Azure Regions](https://azure.microsoft.com/regions/) (https://azure.microsoft.com/regions/#services) in the Azure library.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a99-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="82a99-124">-Profile</span></span>
<span data-ttu-id="82a99-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="82a99-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82a99-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="82a99-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82a99-127">-版本</span><span class="sxs-lookup"><span data-stu-id="82a99-127">-Version</span></span>
<span data-ttu-id="82a99-128">指定新伺服器的版本。</span><span class="sxs-lookup"><span data-stu-id="82a99-128">Specifies the version of the new server.</span></span>
<span data-ttu-id="82a99-129">有效值為：2.0 和12.0。</span><span class="sxs-lookup"><span data-stu-id="82a99-129">Valid values are: 2.0 and 12.0.</span></span>

```yaml
Type: Single
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a99-130">-確認</span><span class="sxs-lookup"><span data-stu-id="82a99-130">-Confirm</span></span>
<span data-ttu-id="82a99-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="82a99-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a99-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82a99-132">-WhatIf</span></span>
<span data-ttu-id="82a99-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82a99-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82a99-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82a99-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a99-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a99-135">CommonParameters</span></span>
<span data-ttu-id="82a99-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82a99-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a99-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82a99-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a99-138">輸入</span><span class="sxs-lookup"><span data-stu-id="82a99-138">INPUTS</span></span>

## <span data-ttu-id="82a99-139">輸出</span><span class="sxs-lookup"><span data-stu-id="82a99-139">OUTPUTS</span></span>

### <span data-ttu-id="82a99-140">WindowsAzure. SqlDatabase. SqlDatabaseServerCoNtext</span><span class="sxs-lookup"><span data-stu-id="82a99-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="82a99-141">筆記</span><span class="sxs-lookup"><span data-stu-id="82a99-141">NOTES</span></span>

## <span data-ttu-id="82a99-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="82a99-142">RELATED LINKS</span></span>

[<span data-ttu-id="82a99-143">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="82a99-143">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="82a99-144">建立伺服器</span><span class="sxs-lookup"><span data-stu-id="82a99-144">Create Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505699.aspx)

[<span data-ttu-id="82a99-145">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="82a99-145">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="82a99-146">AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="82a99-146">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="82a99-147">移除-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="82a99-147">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="82a99-148">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="82a99-148">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


