---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 8e5041b57c4063a3d1ceb2f62e0149132c21b953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452640"
---
# <span data-ttu-id="c5d6e-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c5d6e-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="c5d6e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d6e-103">測試 Analysis Services 伺服器實例是否存在</span><span class="sxs-lookup"><span data-stu-id="c5d6e-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5d6e-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5d6e-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5d6e-105">說明</span><span class="sxs-lookup"><span data-stu-id="c5d6e-105">DESCRIPTION</span></span>
<span data-ttu-id="c5d6e-106">Test-AzureRmAnalysisServicesServer Cmdlet 會測試 Analysis Services 伺服器實例是否存在</span><span class="sxs-lookup"><span data-stu-id="c5d6e-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="c5d6e-107">示例</span><span class="sxs-lookup"><span data-stu-id="c5d6e-107">EXAMPLES</span></span>

### <span data-ttu-id="c5d6e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c5d6e-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="c5d6e-109">這個命令會在 resourcegroup testgroup 中測試是否有一個名為 testserver 的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5d6e-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="c5d6e-110">參數</span><span class="sxs-lookup"><span data-stu-id="c5d6e-110">PARAMETERS</span></span>

### <span data-ttu-id="c5d6e-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="c5d6e-111">-Name</span></span>
<span data-ttu-id="c5d6e-112">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="c5d6e-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="c5d6e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d6e-113">-ResourceGroupName</span></span>
<span data-ttu-id="c5d6e-114">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c5d6e-114">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="c5d6e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d6e-115">-DefaultProfile</span></span>
<span data-ttu-id="c5d6e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5d6e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5d6e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d6e-117">CommonParameters</span></span>
<span data-ttu-id="c5d6e-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5d6e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d6e-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5d6e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d6e-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c5d6e-120">INPUTS</span></span>

## <span data-ttu-id="c5d6e-121">輸出</span><span class="sxs-lookup"><span data-stu-id="c5d6e-121">OUTPUTS</span></span>

### <span data-ttu-id="c5d6e-122">System.object</span><span class="sxs-lookup"><span data-stu-id="c5d6e-122">System.Boolean</span></span>

## <span data-ttu-id="c5d6e-123">筆記</span><span class="sxs-lookup"><span data-stu-id="c5d6e-123">NOTES</span></span>
<span data-ttu-id="c5d6e-124">別名： Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="c5d6e-124">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="c5d6e-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5d6e-125">RELATED LINKS</span></span>

[<span data-ttu-id="c5d6e-126">AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c5d6e-126">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="c5d6e-127">移除-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c5d6e-127">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
