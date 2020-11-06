---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: 48b1ee50f1ebd0003097500849a6d03dac64c2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457235"
---
# <span data-ttu-id="3d783-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3d783-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="3d783-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d783-102">SYNOPSIS</span></span>
<span data-ttu-id="3d783-103">移除 Azure SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d783-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d783-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d783-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d783-105">說明</span><span class="sxs-lookup"><span data-stu-id="3d783-105">DESCRIPTION</span></span>
<span data-ttu-id="3d783-106">**AzureRmSqlServer** Cmdlet 會移除 Azure SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d783-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>

<span data-ttu-id="3d783-107">[刪除] 作業是非同步作業，可能需要一些時間，所以請在執行任何其他操作（取決於要完全刪除的伺服器）之前，先確認該作業已完成。</span><span class="sxs-lookup"><span data-stu-id="3d783-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="3d783-108">例如，您需要建立一個使用相同名稱的新伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d783-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="3d783-109">示例</span><span class="sxs-lookup"><span data-stu-id="3d783-109">EXAMPLES</span></span>

### <span data-ttu-id="3d783-110">範例1：移除伺服器</span><span class="sxs-lookup"><span data-stu-id="3d783-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="3d783-111">這個命令會移除名為 Server01 的 Azure SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d783-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="3d783-112">參數</span><span class="sxs-lookup"><span data-stu-id="3d783-112">PARAMETERS</span></span>

### <span data-ttu-id="3d783-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3d783-113">-Force</span></span>
<span data-ttu-id="3d783-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3d783-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3d783-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d783-115">-ResourceGroupName</span></span>
<span data-ttu-id="3d783-116">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d783-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3d783-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3d783-117">-ServerName</span></span>
<span data-ttu-id="3d783-118">指定要移除的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3d783-118">Specifies the name of the server to remove.</span></span>

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

### <span data-ttu-id="3d783-119">-確認</span><span class="sxs-lookup"><span data-stu-id="3d783-119">-Confirm</span></span>
<span data-ttu-id="3d783-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3d783-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d783-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d783-121">-WhatIf</span></span>
<span data-ttu-id="3d783-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d783-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d783-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d783-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d783-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d783-124">-DefaultProfile</span></span>
<span data-ttu-id="3d783-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d783-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d783-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d783-126">CommonParameters</span></span>
<span data-ttu-id="3d783-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d783-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d783-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d783-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d783-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3d783-129">INPUTS</span></span>

### <span data-ttu-id="3d783-130">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="3d783-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="3d783-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3d783-131">OUTPUTS</span></span>

### <span data-ttu-id="3d783-132">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="3d783-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="3d783-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3d783-133">NOTES</span></span>

## <span data-ttu-id="3d783-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d783-134">RELATED LINKS</span></span>

[<span data-ttu-id="3d783-135">AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3d783-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="3d783-136">新-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3d783-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="3d783-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3d783-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="3d783-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="3d783-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


