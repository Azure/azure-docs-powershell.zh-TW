---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 1cb77a435ee951e2e7fe4bc7401e7e4385557eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453236"
---
# <span data-ttu-id="690fd-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="690fd-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="690fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="690fd-102">SYNOPSIS</span></span>
<span data-ttu-id="690fd-103">取得伺服器的威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="690fd-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="690fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="690fd-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="690fd-105">說明</span><span class="sxs-lookup"><span data-stu-id="690fd-105">DESCRIPTION</span></span>
<span data-ttu-id="690fd-106">**AzureRmSqlServerThreatDetectionPolicy** Cmdlet 會取得 Azure SQL server 的威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="690fd-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="690fd-107">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 和 *ServerName* 參數來識別這個 Cmdlet 取得原則的伺服器。</span><span class="sxs-lookup"><span data-stu-id="690fd-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="690fd-108">示例</span><span class="sxs-lookup"><span data-stu-id="690fd-108">EXAMPLES</span></span>

### <span data-ttu-id="690fd-109">範例1：取得伺服器的威脅偵測原則</span><span class="sxs-lookup"><span data-stu-id="690fd-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="690fd-110">這個命令會取得名為 Server01 的伺服器的威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="690fd-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="690fd-111">伺服器已指派給資源群組 ResourceGroup11。</span><span class="sxs-lookup"><span data-stu-id="690fd-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="690fd-112">參數</span><span class="sxs-lookup"><span data-stu-id="690fd-112">PARAMETERS</span></span>

### <span data-ttu-id="690fd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="690fd-113">-ResourceGroupName</span></span>
<span data-ttu-id="690fd-114">指定伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="690fd-114">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="690fd-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="690fd-115">-ServerName</span></span>
<span data-ttu-id="690fd-116">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="690fd-116">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="690fd-117">-確認</span><span class="sxs-lookup"><span data-stu-id="690fd-117">-Confirm</span></span>
<span data-ttu-id="690fd-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="690fd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="690fd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="690fd-119">-WhatIf</span></span>
<span data-ttu-id="690fd-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="690fd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="690fd-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="690fd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="690fd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690fd-122">-DefaultProfile</span></span>
<span data-ttu-id="690fd-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="690fd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="690fd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690fd-124">CommonParameters</span></span>
<span data-ttu-id="690fd-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="690fd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690fd-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="690fd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690fd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="690fd-127">INPUTS</span></span>

## <span data-ttu-id="690fd-128">輸出</span><span class="sxs-lookup"><span data-stu-id="690fd-128">OUTPUTS</span></span>

### <span data-ttu-id="690fd-129">ServerThreatDetectionPolicyModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="690fd-129">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="690fd-130">筆記</span><span class="sxs-lookup"><span data-stu-id="690fd-130">NOTES</span></span>

## <span data-ttu-id="690fd-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="690fd-131">RELATED LINKS</span></span>

[<span data-ttu-id="690fd-132">移除-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="690fd-132">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="690fd-133">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="690fd-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


