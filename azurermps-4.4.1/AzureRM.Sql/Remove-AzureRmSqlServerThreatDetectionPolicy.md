---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: e6a47578ef2442e6ca2f6d03284624f1f2906e35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447118"
---
# <span data-ttu-id="177aa-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="177aa-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="177aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="177aa-102">SYNOPSIS</span></span>
<span data-ttu-id="177aa-103">從伺服器移除威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="177aa-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="177aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="177aa-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="177aa-105">說明</span><span class="sxs-lookup"><span data-stu-id="177aa-105">DESCRIPTION</span></span>
<span data-ttu-id="177aa-106">Remove-AzureRmSqlServerThreatDetectionPolicy Cmdlet 會從 Azure SQL server 中移除威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="177aa-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>

<span data-ttu-id="177aa-107">若要使用這個 Cmdlet，請指定 ResourceGroupName 和 ServerName 參數來識別這個 Cmdlet 移除原則的伺服器。</span><span class="sxs-lookup"><span data-stu-id="177aa-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="177aa-108">示例</span><span class="sxs-lookup"><span data-stu-id="177aa-108">EXAMPLES</span></span>

### <span data-ttu-id="177aa-109">--------------------------範例1：移除資料庫的威脅偵測原則--------------------------</span><span class="sxs-lookup"><span data-stu-id="177aa-109">--------------------------  Example 1: Remove a threat detection policy for a database  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="177aa-110">這個命令會從名為 Server01 的伺服器中移除威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="177aa-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="177aa-111">參數</span><span class="sxs-lookup"><span data-stu-id="177aa-111">PARAMETERS</span></span>

### <span data-ttu-id="177aa-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="177aa-112">-PassThru</span></span>
<span data-ttu-id="177aa-113">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="177aa-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="177aa-114">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="177aa-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="177aa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="177aa-115">-ResourceGroupName</span></span>
<span data-ttu-id="177aa-116">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="177aa-116">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="177aa-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="177aa-117">-ServerName</span></span>
<span data-ttu-id="177aa-118">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="177aa-118">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="177aa-119">-確認</span><span class="sxs-lookup"><span data-stu-id="177aa-119">-Confirm</span></span>
<span data-ttu-id="177aa-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="177aa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="177aa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="177aa-121">-WhatIf</span></span>
<span data-ttu-id="177aa-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="177aa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="177aa-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="177aa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="177aa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="177aa-124">-DefaultProfile</span></span>
<span data-ttu-id="177aa-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="177aa-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="177aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="177aa-126">CommonParameters</span></span>
<span data-ttu-id="177aa-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="177aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="177aa-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="177aa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="177aa-129">輸入</span><span class="sxs-lookup"><span data-stu-id="177aa-129">INPUTS</span></span>

###  
<span data-ttu-id="177aa-130">您無法將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="177aa-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="177aa-131">輸出</span><span class="sxs-lookup"><span data-stu-id="177aa-131">OUTPUTS</span></span>

### <span data-ttu-id="177aa-132">ServerThreatDetectionPolicyModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="177aa-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="177aa-133">這個 Cmdlet 會傳回 ServerThreatDetectionPolicyModel 物件。</span><span class="sxs-lookup"><span data-stu-id="177aa-133">This cmdlet returns a ServerThreatDetectionPolicyModel object.</span></span>

## <span data-ttu-id="177aa-134">筆記</span><span class="sxs-lookup"><span data-stu-id="177aa-134">NOTES</span></span>

## <span data-ttu-id="177aa-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="177aa-135">RELATED LINKS</span></span>

[<span data-ttu-id="177aa-136">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="177aa-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

