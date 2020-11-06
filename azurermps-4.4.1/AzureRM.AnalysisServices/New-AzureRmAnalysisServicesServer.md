---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0093393f926af257e07b7d697a7f267fa62b483a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445240"
---
# <span data-ttu-id="f3983-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f3983-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="f3983-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3983-102">SYNOPSIS</span></span>
<span data-ttu-id="f3983-103">建立新的 Analysis Services 伺服器</span><span class="sxs-lookup"><span data-stu-id="f3983-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3983-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3983-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3983-105">說明</span><span class="sxs-lookup"><span data-stu-id="f3983-105">DESCRIPTION</span></span>
<span data-ttu-id="f3983-106">New-AzureRmAnalysisServicesServer Cmdlet 會建立新的 Analysis Services 伺服器</span><span class="sxs-lookup"><span data-stu-id="f3983-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="f3983-107">示例</span><span class="sxs-lookup"><span data-stu-id="f3983-107">EXAMPLES</span></span>

### <span data-ttu-id="f3983-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f3983-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="f3983-109">在 Azure 地區的 [美國] 和 [資源群組] testresrourcegroup 中建立名為 testserver 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="f3983-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="f3983-110">伺服器的 sku 層級將是 S1。</span><span class="sxs-lookup"><span data-stu-id="f3983-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="f3983-111">參數</span><span class="sxs-lookup"><span data-stu-id="f3983-111">PARAMETERS</span></span>

### <span data-ttu-id="f3983-112">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="f3983-112">-Administrator</span></span>
<span data-ttu-id="f3983-113">代表要在伺服器上設定為系統管理員之以逗號分隔的使用者或群組清單字串。</span><span class="sxs-lookup"><span data-stu-id="f3983-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="f3983-114">使用者或群組必須指定 UPN 格式，例如 user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f3983-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3983-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="f3983-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="f3983-116">用於備份 Analysis Services 伺服器的 blob 容器 Uri</span><span class="sxs-lookup"><span data-stu-id="f3983-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3983-117">-位置</span><span class="sxs-lookup"><span data-stu-id="f3983-117">-Location</span></span>
<span data-ttu-id="f3983-118">託管分析服務伺服器的 Azure 區域</span><span class="sxs-lookup"><span data-stu-id="f3983-118">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: North Central US, South Central US, Central US, West Europe, North Europe, West US, East US, East US 2, Japan East, Japan West, Brazil South, Southeast Asia, East Asia, Australia East, Australia Southeast

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3983-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3983-119">-Name</span></span>
<span data-ttu-id="f3983-120">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="f3983-120">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3983-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3983-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3983-122">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="f3983-122">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3983-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="f3983-123">-Sku</span></span>
<span data-ttu-id="f3983-124">伺服器 Sku 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3983-124">The name of the Sku for the server.</span></span>
<span data-ttu-id="f3983-125">受支援的值為標準層級的 0 "，" 1 "，" 2 "，"，"2"，"4";[B1 "，" B2 "代表 [基本層]，[中的 1" 代表開發層。</span><span class="sxs-lookup"><span data-stu-id="f3983-125">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3983-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="f3983-126">-Tag</span></span>
<span data-ttu-id="f3983-127">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="f3983-127">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3983-128">-確認</span><span class="sxs-lookup"><span data-stu-id="f3983-128">-Confirm</span></span>
<span data-ttu-id="f3983-129">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="f3983-129">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="f3983-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3983-130">-WhatIf</span></span>
<span data-ttu-id="f3983-131">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="f3983-131">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="f3983-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3983-132">CommonParameters</span></span>
<span data-ttu-id="f3983-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3983-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3983-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3983-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3983-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f3983-135">INPUTS</span></span>

## <span data-ttu-id="f3983-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f3983-136">OUTPUTS</span></span>

### <span data-ttu-id="f3983-137">AzureAnalysisServicesServer 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="f3983-137">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="f3983-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f3983-138">NOTES</span></span>
<span data-ttu-id="f3983-139">別名： New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="f3983-139">Alias: New-AzureAs</span></span>

## <span data-ttu-id="f3983-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3983-140">RELATED LINKS</span></span>

[<span data-ttu-id="f3983-141">AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f3983-141">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="f3983-142">移除-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f3983-142">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
