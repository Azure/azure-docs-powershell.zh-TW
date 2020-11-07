---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: 5354737602f168245d6c4c8dca560698fa6cfac2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626517"
---
# <span data-ttu-id="f17e1-101">Export-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="f17e1-101">Export-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="f17e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f17e1-102">SYNOPSIS</span></span>
<span data-ttu-id="f17e1-103">根據 Add-AzureAnalysisServicesAccount 命令中指定的，從目前登入的環境中的 Analysis Services 伺服器實例匯出記錄</span><span class="sxs-lookup"><span data-stu-id="f17e1-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f17e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f17e1-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## <span data-ttu-id="f17e1-105">說明</span><span class="sxs-lookup"><span data-stu-id="f17e1-105">DESCRIPTION</span></span>
<span data-ttu-id="f17e1-106">Export-AzureAnalysisServicesInstance Cmdlet 會將來自 Azure Analysis Services 伺服器實例的記錄匯出至檔案</span><span class="sxs-lookup"><span data-stu-id="f17e1-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="f17e1-107">示例</span><span class="sxs-lookup"><span data-stu-id="f17e1-107">EXAMPLES</span></span>

### <span data-ttu-id="f17e1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f17e1-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="f17e1-109">這個命令會從 [Add-AzureAnalysisServicesAccount] 命令指定之環境中的伺服器 ' testserver」匯出記錄，並將其儲存到 OutputPath ' C:\path\to\log\testserver.log」中指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="f17e1-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="f17e1-110">參數</span><span class="sxs-lookup"><span data-stu-id="f17e1-110">PARAMETERS</span></span>

### <span data-ttu-id="f17e1-111">-實例</span><span class="sxs-lookup"><span data-stu-id="f17e1-111">-Instance</span></span>
<span data-ttu-id="f17e1-112">Analysis Services 伺服器實例的名稱</span><span class="sxs-lookup"><span data-stu-id="f17e1-112">Name of the Analysis Services server instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17e1-113">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="f17e1-113">-OutputPath</span></span>
<span data-ttu-id="f17e1-114">匯出記錄至檔案的輸出路徑</span><span class="sxs-lookup"><span data-stu-id="f17e1-114">Output path to file to export log</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17e1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f17e1-115">-Force</span></span>
<span data-ttu-id="f17e1-116">覆蓋檔案（如果有的話）而不詢問</span><span class="sxs-lookup"><span data-stu-id="f17e1-116">Overwrite file if exists without asking</span></span>

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

## <span data-ttu-id="f17e1-117">輸入</span><span class="sxs-lookup"><span data-stu-id="f17e1-117">INPUTS</span></span>

## <span data-ttu-id="f17e1-118">輸出</span><span class="sxs-lookup"><span data-stu-id="f17e1-118">OUTPUTS</span></span>

## <span data-ttu-id="f17e1-119">筆記</span><span class="sxs-lookup"><span data-stu-id="f17e1-119">NOTES</span></span>
<span data-ttu-id="f17e1-120">別名： Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="f17e1-120">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="f17e1-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="f17e1-121">RELATED LINKS</span></span>

