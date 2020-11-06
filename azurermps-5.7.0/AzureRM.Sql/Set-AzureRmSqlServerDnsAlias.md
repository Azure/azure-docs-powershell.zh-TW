---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 78ffcb50b47b315426998825232348dd41c23f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445971"
---
# <span data-ttu-id="24618-101">Set-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="24618-101">Set-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="24618-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24618-102">SYNOPSIS</span></span>
<span data-ttu-id="24618-103">修改 Azure SQL Server DNS 別名指向的目標伺服器</span><span class="sxs-lookup"><span data-stu-id="24618-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24618-104">句法</span><span class="sxs-lookup"><span data-stu-id="24618-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24618-105">說明</span><span class="sxs-lookup"><span data-stu-id="24618-105">DESCRIPTION</span></span>
<span data-ttu-id="24618-106">這個命令正在更新別名指向哪個伺服器。</span><span class="sxs-lookup"><span data-stu-id="24618-106">This command is updating the server to which alias is pointing.</span></span> 

<span data-ttu-id="24618-107">此命令必須在登入要指向哪個別名所要指向的新伺服器時發出訂閱。</span><span class="sxs-lookup"><span data-stu-id="24618-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="24618-108">示例</span><span class="sxs-lookup"><span data-stu-id="24618-108">EXAMPLES</span></span>

### <span data-ttu-id="24618-109">範例1</span><span class="sxs-lookup"><span data-stu-id="24618-109">Example 1</span></span>
```
PS C:\> Set-AzureRmSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="24618-110">這個命令正在更新，且先前指向 oldServer 的別名指向 server newServer</span><span class="sxs-lookup"><span data-stu-id="24618-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="24618-111">參數</span><span class="sxs-lookup"><span data-stu-id="24618-111">PARAMETERS</span></span>

### <span data-ttu-id="24618-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24618-112">-AsJob</span></span>
<span data-ttu-id="24618-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24618-113">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="24618-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24618-114">-DefaultProfile</span></span>
<span data-ttu-id="24618-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24618-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24618-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="24618-116">-Name</span></span>
<span data-ttu-id="24618-117">Azure Sql Server Dns 別名名稱。</span><span class="sxs-lookup"><span data-stu-id="24618-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24618-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24618-118">-ResourceGroupName</span></span>
<span data-ttu-id="24618-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24618-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24618-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="24618-120">-SourceServerName</span></span>
<span data-ttu-id="24618-121">別名目前指向哪個 Azure Sql Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="24618-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="24618-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24618-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="24618-123">來源伺服器的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24618-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="24618-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24618-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="24618-125">來源伺服器的訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="24618-125">The subscription id of the source server</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24618-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="24618-126">-TargetServerName</span></span>
<span data-ttu-id="24618-127">別名應該指向哪個 Azure Sql Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="24618-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="24618-128">-確認</span><span class="sxs-lookup"><span data-stu-id="24618-128">-Confirm</span></span>
<span data-ttu-id="24618-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24618-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24618-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24618-130">-WhatIf</span></span>
<span data-ttu-id="24618-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24618-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24618-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24618-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24618-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24618-133">CommonParameters</span></span>
<span data-ttu-id="24618-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24618-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24618-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24618-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24618-136">輸入</span><span class="sxs-lookup"><span data-stu-id="24618-136">INPUTS</span></span>

### <span data-ttu-id="24618-137">System.object</span><span class="sxs-lookup"><span data-stu-id="24618-137">System.String</span></span>

## <span data-ttu-id="24618-138">輸出</span><span class="sxs-lookup"><span data-stu-id="24618-138">OUTPUTS</span></span>

### <span data-ttu-id="24618-139">AzureSqlServerDnsAliasModel 中的 [ServerDnsAlias]</span><span class="sxs-lookup"><span data-stu-id="24618-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="24618-140">筆記</span><span class="sxs-lookup"><span data-stu-id="24618-140">NOTES</span></span>

## <span data-ttu-id="24618-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="24618-141">RELATED LINKS</span></span>
