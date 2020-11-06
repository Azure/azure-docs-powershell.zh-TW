---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 7298612cf64b4f90f65ebaa2943b38102b5ae1ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614090"
---
# <span data-ttu-id="4c4a8-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4c4a8-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="4c4a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c4a8-102">SYNOPSIS</span></span>
<span data-ttu-id="4c4a8-103">測試 Analysis Services 伺服器實例是否存在</span><span class="sxs-lookup"><span data-stu-id="4c4a8-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="4c4a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c4a8-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c4a8-105">說明</span><span class="sxs-lookup"><span data-stu-id="4c4a8-105">DESCRIPTION</span></span>
<span data-ttu-id="4c4a8-106">Test-AzAnalysisServicesServer Cmdlet 會測試 Analysis Services 伺服器實例是否存在</span><span class="sxs-lookup"><span data-stu-id="4c4a8-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="4c4a8-107">示例</span><span class="sxs-lookup"><span data-stu-id="4c4a8-107">EXAMPLES</span></span>

### <span data-ttu-id="4c4a8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4c4a8-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="4c4a8-109">這個命令會在 resourcegroup testgroup 中測試是否有一個名為 testserver 的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c4a8-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="4c4a8-110">參數</span><span class="sxs-lookup"><span data-stu-id="4c4a8-110">PARAMETERS</span></span>

### <span data-ttu-id="4c4a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c4a8-111">-DefaultProfile</span></span>
<span data-ttu-id="4c4a8-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c4a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c4a8-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="4c4a8-113">-Name</span></span>
<span data-ttu-id="4c4a8-114">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="4c4a8-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="4c4a8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c4a8-115">-ResourceGroupName</span></span>
<span data-ttu-id="4c4a8-116">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="4c4a8-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c4a8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c4a8-117">CommonParameters</span></span>
<span data-ttu-id="4c4a8-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c4a8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c4a8-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c4a8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c4a8-120">輸入</span><span class="sxs-lookup"><span data-stu-id="4c4a8-120">INPUTS</span></span>

### <span data-ttu-id="4c4a8-121">System.object</span><span class="sxs-lookup"><span data-stu-id="4c4a8-121">System.String</span></span>

## <span data-ttu-id="4c4a8-122">輸出</span><span class="sxs-lookup"><span data-stu-id="4c4a8-122">OUTPUTS</span></span>

### <span data-ttu-id="4c4a8-123">System.object</span><span class="sxs-lookup"><span data-stu-id="4c4a8-123">System.Boolean</span></span>

## <span data-ttu-id="4c4a8-124">筆記</span><span class="sxs-lookup"><span data-stu-id="4c4a8-124">NOTES</span></span>
<span data-ttu-id="4c4a8-125">別名： Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="4c4a8-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="4c4a8-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c4a8-126">RELATED LINKS</span></span>

[<span data-ttu-id="4c4a8-127">AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4c4a8-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="4c4a8-128">移除-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4c4a8-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)