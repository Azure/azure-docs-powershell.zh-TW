---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5b75c2058fb7a6ddf323ebeaa6aad6967dcb5b01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614766"
---
# <span data-ttu-id="5064f-101">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5064f-101">Remove-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="5064f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5064f-102">SYNOPSIS</span></span>
<span data-ttu-id="5064f-103">從伺服器移除威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="5064f-103">Removes the threat detection policy from a server.</span></span>

## <span data-ttu-id="5064f-104">句法</span><span class="sxs-lookup"><span data-stu-id="5064f-104">SYNTAX</span></span>

```
Remove-AzSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5064f-105">說明</span><span class="sxs-lookup"><span data-stu-id="5064f-105">DESCRIPTION</span></span>
<span data-ttu-id="5064f-106">Remove-AzSqlServerThreatDetectionPolicy Cmdlet 會從 Azure SQL server 中移除威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="5064f-106">The Remove-AzSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>
<span data-ttu-id="5064f-107">若要使用這個 Cmdlet，請指定 ResourceGroupName 和 ServerName 參數來識別這個 Cmdlet 移除原則的伺服器。</span><span class="sxs-lookup"><span data-stu-id="5064f-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="5064f-108">示例</span><span class="sxs-lookup"><span data-stu-id="5064f-108">EXAMPLES</span></span>

### <span data-ttu-id="5064f-109">範例1：移除資料庫的威脅偵測原則</span><span class="sxs-lookup"><span data-stu-id="5064f-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\> Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="5064f-110">這個命令會從名為 Server01 的伺服器中移除威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="5064f-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="5064f-111">參數</span><span class="sxs-lookup"><span data-stu-id="5064f-111">PARAMETERS</span></span>

### <span data-ttu-id="5064f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5064f-112">-DefaultProfile</span></span>
<span data-ttu-id="5064f-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5064f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5064f-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5064f-114">-PassThru</span></span>
<span data-ttu-id="5064f-115">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="5064f-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5064f-116">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5064f-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5064f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5064f-117">-ResourceGroupName</span></span>
<span data-ttu-id="5064f-118">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5064f-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="5064f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5064f-119">-ServerName</span></span>
<span data-ttu-id="5064f-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5064f-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5064f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="5064f-121">-Confirm</span></span>
<span data-ttu-id="5064f-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5064f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5064f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5064f-123">-WhatIf</span></span>
<span data-ttu-id="5064f-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5064f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5064f-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5064f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5064f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5064f-126">CommonParameters</span></span>
<span data-ttu-id="5064f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5064f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5064f-128">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5064f-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5064f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5064f-129">INPUTS</span></span>

### <span data-ttu-id="5064f-130">System.object</span><span class="sxs-lookup"><span data-stu-id="5064f-130">System.String</span></span>

## <span data-ttu-id="5064f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="5064f-131">OUTPUTS</span></span>

### <span data-ttu-id="5064f-132">ServerThreatDetectionPolicyModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="5064f-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="5064f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5064f-133">NOTES</span></span>

## <span data-ttu-id="5064f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5064f-134">RELATED LINKS</span></span>

[<span data-ttu-id="5064f-135">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="5064f-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

