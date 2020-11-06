---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: f8d01165825c63ece34779f58cb94a3f8e0af40c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614874"
---
# <span data-ttu-id="b9e55-101">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b9e55-101">Get-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="b9e55-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9e55-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e55-103">取得伺服器的威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="b9e55-103">Gets the threat detection policy for a server.</span></span>

## <span data-ttu-id="b9e55-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9e55-104">SYNTAX</span></span>

```
Get-AzSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e55-105">說明</span><span class="sxs-lookup"><span data-stu-id="b9e55-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e55-106">**AzSqlServerThreatDetectionPolicy** Cmdlet 會取得 Azure SQL server 的威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="b9e55-106">The **Get-AzSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="b9e55-107">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 和 *ServerName* 參數來識別這個 Cmdlet 取得原則的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b9e55-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="b9e55-108">示例</span><span class="sxs-lookup"><span data-stu-id="b9e55-108">EXAMPLES</span></span>

### <span data-ttu-id="b9e55-109">範例1：取得伺服器的威脅偵測原則</span><span class="sxs-lookup"><span data-stu-id="b9e55-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="b9e55-110">這個命令會取得名為 Server01 的伺服器的威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="b9e55-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="b9e55-111">伺服器已指派給資源群組 ResourceGroup11。</span><span class="sxs-lookup"><span data-stu-id="b9e55-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="b9e55-112">參數</span><span class="sxs-lookup"><span data-stu-id="b9e55-112">PARAMETERS</span></span>

### <span data-ttu-id="b9e55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e55-113">-DefaultProfile</span></span>
<span data-ttu-id="b9e55-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b9e55-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9e55-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e55-115">-ResourceGroupName</span></span>
<span data-ttu-id="b9e55-116">指定伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9e55-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="b9e55-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9e55-117">-ServerName</span></span>
<span data-ttu-id="b9e55-118">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9e55-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b9e55-119">-確認</span><span class="sxs-lookup"><span data-stu-id="b9e55-119">-Confirm</span></span>
<span data-ttu-id="b9e55-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b9e55-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e55-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e55-121">-WhatIf</span></span>
<span data-ttu-id="b9e55-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b9e55-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e55-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9e55-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e55-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e55-124">CommonParameters</span></span>
<span data-ttu-id="b9e55-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9e55-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e55-126">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b9e55-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e55-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b9e55-127">INPUTS</span></span>

### <span data-ttu-id="b9e55-128">System.object</span><span class="sxs-lookup"><span data-stu-id="b9e55-128">System.String</span></span>

## <span data-ttu-id="b9e55-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b9e55-129">OUTPUTS</span></span>

### <span data-ttu-id="b9e55-130">ServerThreatDetectionPolicyModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="b9e55-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="b9e55-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b9e55-131">NOTES</span></span>

## <span data-ttu-id="b9e55-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9e55-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9e55-133">移除-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b9e55-133">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="b9e55-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b9e55-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


