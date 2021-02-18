---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 38388f4a2d1d88ae668b8a6384ca228a9436ac68
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405902"
---
# <span data-ttu-id="23f20-101">Get-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="23f20-101">Get-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="23f20-102">簡介</span><span class="sxs-lookup"><span data-stu-id="23f20-102">SYNOPSIS</span></span>
<span data-ttu-id="23f20-103">為伺服器獲取進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="23f20-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="23f20-104">語法</span><span class="sxs-lookup"><span data-stu-id="23f20-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSettings -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23f20-105">描述</span><span class="sxs-lookup"><span data-stu-id="23f20-105">DESCRIPTION</span></span>
<span data-ttu-id="23f20-106">**Get-AzSqlServerAdvancedThreatProtectionSettings** Cmdlet 會取得 Azure SQL 伺服器進一步的威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="23f20-106">The **Get-AzSqlServerAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="23f20-107">若要使用此 Cmdlet，請指定 *ResourceGroupName* 和 *ServerName* 參數，以識別此 Cmdlet 會獲得設定的伺服器。</span><span class="sxs-lookup"><span data-stu-id="23f20-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="23f20-108">例子</span><span class="sxs-lookup"><span data-stu-id="23f20-108">EXAMPLES</span></span>

### <span data-ttu-id="23f20-109">範例 1：取得伺服器的進一步威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="23f20-109">Example 1: Get the advanced threat protection settings for a server</span></span>
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

<span data-ttu-id="23f20-110">此命令會針對伺服器名稱為 Server01 的進一階段威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="23f20-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="23f20-111">伺服器會指派給資源群組 ResourceGroup11。</span><span class="sxs-lookup"><span data-stu-id="23f20-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="23f20-112">參數</span><span class="sxs-lookup"><span data-stu-id="23f20-112">PARAMETERS</span></span>

### <span data-ttu-id="23f20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f20-113">-DefaultProfile</span></span>
<span data-ttu-id="23f20-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="23f20-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23f20-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f20-115">-ResourceGroupName</span></span>
<span data-ttu-id="23f20-116">指定伺服器所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="23f20-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="23f20-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="23f20-117">-ServerName</span></span>
<span data-ttu-id="23f20-118">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="23f20-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="23f20-119">-確認</span><span class="sxs-lookup"><span data-stu-id="23f20-119">-Confirm</span></span>
<span data-ttu-id="23f20-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="23f20-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f20-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23f20-121">-WhatIf</span></span>
<span data-ttu-id="23f20-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23f20-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23f20-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23f20-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f20-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f20-124">CommonParameters</span></span>
<span data-ttu-id="23f20-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="23f20-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f20-126">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="23f20-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f20-127">輸入</span><span class="sxs-lookup"><span data-stu-id="23f20-127">INPUTS</span></span>

### <span data-ttu-id="23f20-128">System.String</span><span class="sxs-lookup"><span data-stu-id="23f20-128">System.String</span></span>

## <span data-ttu-id="23f20-129">輸出</span><span class="sxs-lookup"><span data-stu-id="23f20-129">OUTPUTS</span></span>

### <span data-ttu-id="23f20-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="23f20-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="23f20-131">筆記</span><span class="sxs-lookup"><span data-stu-id="23f20-131">NOTES</span></span>

## <span data-ttu-id="23f20-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="23f20-132">RELATED LINKS</span></span>


[<span data-ttu-id="23f20-133">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="23f20-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


