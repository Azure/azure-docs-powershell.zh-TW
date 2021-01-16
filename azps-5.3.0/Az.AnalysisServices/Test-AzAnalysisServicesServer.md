---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447692"
---
# <span data-ttu-id="8a34a-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8a34a-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="8a34a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a34a-102">SYNOPSIS</span></span>
<span data-ttu-id="8a34a-103">測試 Analysis Services 伺服器實例是否存在</span><span class="sxs-lookup"><span data-stu-id="8a34a-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="8a34a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a34a-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a34a-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a34a-105">DESCRIPTION</span></span>
<span data-ttu-id="8a34a-106">Test-AzAnalysisServicesServer Cmdlet 會測試 Analysis Services 伺服器實例是否存在</span><span class="sxs-lookup"><span data-stu-id="8a34a-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="8a34a-107">示例</span><span class="sxs-lookup"><span data-stu-id="8a34a-107">EXAMPLES</span></span>

### <span data-ttu-id="8a34a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8a34a-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="8a34a-109">這個命令會在 resourcegroup testgroup 中測試是否有一個名為 testserver 的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a34a-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="8a34a-110">參數</span><span class="sxs-lookup"><span data-stu-id="8a34a-110">PARAMETERS</span></span>

### <span data-ttu-id="8a34a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a34a-111">-DefaultProfile</span></span>
<span data-ttu-id="8a34a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a34a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a34a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a34a-113">-Name</span></span>
<span data-ttu-id="8a34a-114">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="8a34a-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="8a34a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a34a-115">-ResourceGroupName</span></span>
<span data-ttu-id="8a34a-116">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="8a34a-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="8a34a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a34a-117">CommonParameters</span></span>
<span data-ttu-id="8a34a-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a34a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a34a-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8a34a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a34a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="8a34a-120">INPUTS</span></span>

### <span data-ttu-id="8a34a-121">System.object</span><span class="sxs-lookup"><span data-stu-id="8a34a-121">System.String</span></span>

## <span data-ttu-id="8a34a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="8a34a-122">OUTPUTS</span></span>

### <span data-ttu-id="8a34a-123">System.object</span><span class="sxs-lookup"><span data-stu-id="8a34a-123">System.Boolean</span></span>

## <span data-ttu-id="8a34a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="8a34a-124">NOTES</span></span>
<span data-ttu-id="8a34a-125">別名： Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="8a34a-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="8a34a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a34a-126">RELATED LINKS</span></span>

[<span data-ttu-id="8a34a-127">AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8a34a-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="8a34a-128">移除-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8a34a-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
