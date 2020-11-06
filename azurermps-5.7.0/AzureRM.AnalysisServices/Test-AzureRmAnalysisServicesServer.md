---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/test-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 9dd8a86d1e98268708d7b0a12448df109ee083f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456299"
---
# <span data-ttu-id="b40a7-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b40a7-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="b40a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b40a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b40a7-103">測試 Analysis Services 伺服器實例是否存在</span><span class="sxs-lookup"><span data-stu-id="b40a7-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b40a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="b40a7-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b40a7-105">說明</span><span class="sxs-lookup"><span data-stu-id="b40a7-105">DESCRIPTION</span></span>
<span data-ttu-id="b40a7-106">Test-AzureRmAnalysisServicesServer Cmdlet 會測試 Analysis Services 伺服器實例是否存在</span><span class="sxs-lookup"><span data-stu-id="b40a7-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="b40a7-107">示例</span><span class="sxs-lookup"><span data-stu-id="b40a7-107">EXAMPLES</span></span>

### <span data-ttu-id="b40a7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b40a7-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="b40a7-109">這個命令會在 resourcegroup testgroup 中測試是否有一個名為 testserver 的伺服器</span><span class="sxs-lookup"><span data-stu-id="b40a7-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="b40a7-110">參數</span><span class="sxs-lookup"><span data-stu-id="b40a7-110">PARAMETERS</span></span>

### <span data-ttu-id="b40a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b40a7-111">-DefaultProfile</span></span>
<span data-ttu-id="b40a7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b40a7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40a7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b40a7-113">-Name</span></span>
<span data-ttu-id="b40a7-114">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="b40a7-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="b40a7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b40a7-115">-ResourceGroupName</span></span>
<span data-ttu-id="b40a7-116">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="b40a7-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b40a7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b40a7-117">CommonParameters</span></span>
<span data-ttu-id="b40a7-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b40a7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b40a7-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b40a7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b40a7-120">輸入</span><span class="sxs-lookup"><span data-stu-id="b40a7-120">INPUTS</span></span>

### <span data-ttu-id="b40a7-121">所有</span><span class="sxs-lookup"><span data-stu-id="b40a7-121">None</span></span>
<span data-ttu-id="b40a7-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b40a7-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b40a7-123">輸出</span><span class="sxs-lookup"><span data-stu-id="b40a7-123">OUTPUTS</span></span>

### <span data-ttu-id="b40a7-124">System.object</span><span class="sxs-lookup"><span data-stu-id="b40a7-124">System.Boolean</span></span>

## <span data-ttu-id="b40a7-125">筆記</span><span class="sxs-lookup"><span data-stu-id="b40a7-125">NOTES</span></span>
<span data-ttu-id="b40a7-126">別名： Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="b40a7-126">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="b40a7-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b40a7-127">RELATED LINKS</span></span>

[<span data-ttu-id="b40a7-128">AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b40a7-128">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="b40a7-129">移除-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b40a7-129">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
