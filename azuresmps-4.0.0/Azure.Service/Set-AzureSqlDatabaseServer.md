---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967310"
---
# <span data-ttu-id="1e02e-101">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1e02e-101">Set-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="1e02e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e02e-102">SYNOPSIS</span></span>
<span data-ttu-id="1e02e-103">修改 Azure SQL 資料庫伺服器的屬性。</span><span class="sxs-lookup"><span data-stu-id="1e02e-103">Modifies the properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="1e02e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e02e-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e02e-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e02e-105">DESCRIPTION</span></span>
<span data-ttu-id="1e02e-106">**AzureSqlDatabaseServer** Cmdlet 會修改 Azure SQL Database Server 的指定實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="1e02e-106">The **Set-AzureSqlDatabaseServer** cmdlet modifies the properties of the specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="1e02e-107">在目前版本中，您只能補救伺服器的系統管理員帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="1e02e-107">In the current release, you can only update the administrator account password for a server.</span></span>

## <span data-ttu-id="1e02e-108">示例</span><span class="sxs-lookup"><span data-stu-id="1e02e-108">EXAMPLES</span></span>

### <span data-ttu-id="1e02e-109">範例1：變更伺服器的密碼</span><span class="sxs-lookup"><span data-stu-id="1e02e-109">Example 1: Change the password for a server</span></span>
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

<span data-ttu-id="1e02e-110">這個命令會變更名為 lpqd0zbr8y 的 Azure SQL Database 伺服器的系統管理員帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="1e02e-110">This command changes the administrator account password for the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="1e02e-111">參數</span><span class="sxs-lookup"><span data-stu-id="1e02e-111">PARAMETERS</span></span>

### <span data-ttu-id="1e02e-112">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="1e02e-112">-AdminPassword</span></span>
<span data-ttu-id="1e02e-113">指定 Azure SQL 資料庫伺服器的系統管理員帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="1e02e-113">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="1e02e-114">您必須指定強式密碼。</span><span class="sxs-lookup"><span data-stu-id="1e02e-114">You must specify a strong password.</span></span>
<span data-ttu-id="1e02e-115">如需詳細資訊， [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152)請參閱 https://go.microsoft.com/fwlink/p/?LinkId=154152) 在 Microsoft 開發人員網路上 (強式密碼。</span><span class="sxs-lookup"><span data-stu-id="1e02e-115">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="1e02e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1e02e-116">-Force</span></span>
<span data-ttu-id="1e02e-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1e02e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1e02e-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1e02e-118">-Profile</span></span>
<span data-ttu-id="1e02e-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1e02e-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e02e-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1e02e-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e02e-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1e02e-121">-ServerName</span></span>
<span data-ttu-id="1e02e-122">指定此 Cmdlet 修改的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1e02e-122">Specifies the name of the server that this cmdlet modifies.</span></span>
<span data-ttu-id="1e02e-123">指定 [伺服器名稱]，而不是 [完全限定的 DNS 名稱]。</span><span class="sxs-lookup"><span data-stu-id="1e02e-123">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e02e-124">-確認</span><span class="sxs-lookup"><span data-stu-id="1e02e-124">-Confirm</span></span>
<span data-ttu-id="1e02e-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e02e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e02e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e02e-126">-WhatIf</span></span>
<span data-ttu-id="1e02e-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e02e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e02e-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e02e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e02e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e02e-129">CommonParameters</span></span>
<span data-ttu-id="1e02e-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e02e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e02e-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e02e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e02e-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1e02e-132">INPUTS</span></span>

### <span data-ttu-id="1e02e-133">WindowsAzure. SqlDatabase. SqlDatabaseServerCoNtext</span><span class="sxs-lookup"><span data-stu-id="1e02e-133">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="1e02e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1e02e-134">OUTPUTS</span></span>

## <span data-ttu-id="1e02e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="1e02e-135">NOTES</span></span>

## <span data-ttu-id="1e02e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e02e-136">RELATED LINKS</span></span>

[<span data-ttu-id="1e02e-137">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="1e02e-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="1e02e-138">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="1e02e-138">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="1e02e-139">AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1e02e-139">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="1e02e-140">新-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1e02e-140">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="1e02e-141">移除-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1e02e-141">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)


