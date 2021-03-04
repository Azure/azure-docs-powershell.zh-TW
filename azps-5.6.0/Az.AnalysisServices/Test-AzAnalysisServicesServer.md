---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: cb6680276359fddcf9a98cde3e90cb44185c4e85
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903725"
---
# <span data-ttu-id="a201b-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a201b-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="a201b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a201b-102">SYNOPSIS</span></span>
<span data-ttu-id="a201b-103">測試 Analysis Services 伺服器實例是否存在</span><span class="sxs-lookup"><span data-stu-id="a201b-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="a201b-104">語法</span><span class="sxs-lookup"><span data-stu-id="a201b-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a201b-105">描述</span><span class="sxs-lookup"><span data-stu-id="a201b-105">DESCRIPTION</span></span>
<span data-ttu-id="a201b-106">此Test-AzAnalysisServicesServer Cmdlet 會測試 Analysis Services 伺服器實例是否存在</span><span class="sxs-lookup"><span data-stu-id="a201b-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="a201b-107">例子</span><span class="sxs-lookup"><span data-stu-id="a201b-107">EXAMPLES</span></span>

### <span data-ttu-id="a201b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a201b-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="a201b-109">此命令會測試資源組測試組中是否有名為 testerver 的伺服器</span><span class="sxs-lookup"><span data-stu-id="a201b-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="a201b-110">參數</span><span class="sxs-lookup"><span data-stu-id="a201b-110">PARAMETERS</span></span>

### <span data-ttu-id="a201b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a201b-111">-DefaultProfile</span></span>
<span data-ttu-id="a201b-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a201b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a201b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a201b-113">-Name</span></span>
<span data-ttu-id="a201b-114">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="a201b-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="a201b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a201b-115">-ResourceGroupName</span></span>
<span data-ttu-id="a201b-116">伺服器所屬的 Azure 資源組名</span><span class="sxs-lookup"><span data-stu-id="a201b-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="a201b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a201b-117">CommonParameters</span></span>
<span data-ttu-id="a201b-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a201b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a201b-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a201b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a201b-120">輸入</span><span class="sxs-lookup"><span data-stu-id="a201b-120">INPUTS</span></span>

### <span data-ttu-id="a201b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a201b-121">System.String</span></span>

## <span data-ttu-id="a201b-122">輸出</span><span class="sxs-lookup"><span data-stu-id="a201b-122">OUTPUTS</span></span>

### <span data-ttu-id="a201b-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a201b-123">System.Boolean</span></span>

## <span data-ttu-id="a201b-124">筆記</span><span class="sxs-lookup"><span data-stu-id="a201b-124">NOTES</span></span>
<span data-ttu-id="a201b-125">別名：Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="a201b-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="a201b-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a201b-126">RELATED LINKS</span></span>

[<span data-ttu-id="a201b-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a201b-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="a201b-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a201b-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
