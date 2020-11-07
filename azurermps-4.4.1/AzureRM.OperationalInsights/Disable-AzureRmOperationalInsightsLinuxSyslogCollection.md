---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 921465be93701cbf19b30c661df5a5e3d04413d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624794"
---
# <span data-ttu-id="313a7-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="313a7-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="313a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="313a7-102">SYNOPSIS</span></span>
<span data-ttu-id="313a7-103">停止從 Linux 電腦收集 syslog 資料。</span><span class="sxs-lookup"><span data-stu-id="313a7-103">Stops collection of syslog data from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="313a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="313a7-104">SYNTAX</span></span>

### <span data-ttu-id="313a7-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="313a7-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="313a7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="313a7-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="313a7-107">說明</span><span class="sxs-lookup"><span data-stu-id="313a7-107">DESCRIPTION</span></span>
<span data-ttu-id="313a7-108">**Disable AzureRmOperationalInsightsLinuxSyslogCollection** Cmdlet 會在工作區中停止從已連接的 Linux 電腦收集 syslog 資料。</span><span class="sxs-lookup"><span data-stu-id="313a7-108">The **Disable-AzureRmOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="313a7-109">示例</span><span class="sxs-lookup"><span data-stu-id="313a7-109">EXAMPLES</span></span>

## <span data-ttu-id="313a7-110">參數</span><span class="sxs-lookup"><span data-stu-id="313a7-110">PARAMETERS</span></span>

### <span data-ttu-id="313a7-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="313a7-111">-ResourceGroupName</span></span>
<span data-ttu-id="313a7-112">指定包含 Linux 電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="313a7-112">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="313a7-113">-工作區</span><span class="sxs-lookup"><span data-stu-id="313a7-113">-Workspace</span></span>
<span data-ttu-id="313a7-114">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="313a7-114">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="313a7-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="313a7-115">-WorkspaceName</span></span>
<span data-ttu-id="313a7-116">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="313a7-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="313a7-117">-確認</span><span class="sxs-lookup"><span data-stu-id="313a7-117">-Confirm</span></span>
<span data-ttu-id="313a7-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="313a7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="313a7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="313a7-119">-WhatIf</span></span>
<span data-ttu-id="313a7-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="313a7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="313a7-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="313a7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="313a7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313a7-122">-DefaultProfile</span></span>
<span data-ttu-id="313a7-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="313a7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="313a7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313a7-124">CommonParameters</span></span>
<span data-ttu-id="313a7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="313a7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313a7-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="313a7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313a7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="313a7-127">INPUTS</span></span>

### <span data-ttu-id="313a7-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="313a7-128">PSWorkspace</span></span>
<span data-ttu-id="313a7-129">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="313a7-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="313a7-130">輸出</span><span class="sxs-lookup"><span data-stu-id="313a7-130">OUTPUTS</span></span>

### <span data-ttu-id="313a7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="313a7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="313a7-132">筆記</span><span class="sxs-lookup"><span data-stu-id="313a7-132">NOTES</span></span>
* <span data-ttu-id="313a7-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="313a7-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="313a7-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="313a7-134">RELATED LINKS</span></span>

[<span data-ttu-id="313a7-135">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="313a7-135">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="313a7-136">新-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="313a7-136">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


