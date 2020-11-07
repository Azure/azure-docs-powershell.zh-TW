---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 1895fe45f51782cc1a3a54d8b2d0f2da752c2990
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792478"
---
# <span data-ttu-id="2e0dd-101">Get-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="2e0dd-101">Get-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="2e0dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e0dd-102">SYNOPSIS</span></span>
<span data-ttu-id="2e0dd-103">取得伺服器的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="2e0dd-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="2e0dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e0dd-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSettings -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e0dd-105">說明</span><span class="sxs-lookup"><span data-stu-id="2e0dd-105">DESCRIPTION</span></span>
<span data-ttu-id="2e0dd-106">**AzSqlServerAdvancedThreatProtectionSettings** Cmdlet 會取得 Azure SQL server 的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="2e0dd-106">The **Get-AzSqlServerAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="2e0dd-107">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 和 *ServerName* 參數來識別這個 Cmdlet 取得其設定的伺服器。</span><span class="sxs-lookup"><span data-stu-id="2e0dd-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="2e0dd-108">示例</span><span class="sxs-lookup"><span data-stu-id="2e0dd-108">EXAMPLES</span></span>

### <span data-ttu-id="2e0dd-109">範例1：取得伺服器的高級威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="2e0dd-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="2e0dd-110">這個命令會取得名為 Server01 的伺服器的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="2e0dd-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="2e0dd-111">伺服器已指派給資源群組 ResourceGroup11。</span><span class="sxs-lookup"><span data-stu-id="2e0dd-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="2e0dd-112">參數</span><span class="sxs-lookup"><span data-stu-id="2e0dd-112">PARAMETERS</span></span>

### <span data-ttu-id="2e0dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e0dd-113">-DefaultProfile</span></span>
<span data-ttu-id="2e0dd-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2e0dd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e0dd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e0dd-115">-ResourceGroupName</span></span>
<span data-ttu-id="2e0dd-116">指定伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e0dd-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="2e0dd-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2e0dd-117">-ServerName</span></span>
<span data-ttu-id="2e0dd-118">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e0dd-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="2e0dd-119">-確認</span><span class="sxs-lookup"><span data-stu-id="2e0dd-119">-Confirm</span></span>
<span data-ttu-id="2e0dd-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2e0dd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e0dd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e0dd-121">-WhatIf</span></span>
<span data-ttu-id="2e0dd-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e0dd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e0dd-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e0dd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e0dd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e0dd-124">CommonParameters</span></span>
<span data-ttu-id="2e0dd-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e0dd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e0dd-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e0dd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e0dd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2e0dd-127">INPUTS</span></span>

### <span data-ttu-id="2e0dd-128">System.object</span><span class="sxs-lookup"><span data-stu-id="2e0dd-128">System.String</span></span>

## <span data-ttu-id="2e0dd-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2e0dd-129">OUTPUTS</span></span>

### <span data-ttu-id="2e0dd-130">ServerAdvancedThreatProtectionSettingsModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="2e0dd-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="2e0dd-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2e0dd-131">NOTES</span></span>

## <span data-ttu-id="2e0dd-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e0dd-132">RELATED LINKS</span></span>

[<span data-ttu-id="2e0dd-133">移除-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="2e0dd-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSettings.md)

[<span data-ttu-id="2e0dd-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="2e0dd-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


