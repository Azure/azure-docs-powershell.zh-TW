---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 4aedbb502780a08d0ce5556af84a445ab44552f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795330"
---
# <span data-ttu-id="cdbbe-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="cdbbe-101">Get-AzLocation</span></span>

## <span data-ttu-id="cdbbe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cdbbe-102">SYNOPSIS</span></span>
<span data-ttu-id="cdbbe-103">取得每個位置的所有位置和支援的資源提供者。</span><span class="sxs-lookup"><span data-stu-id="cdbbe-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="cdbbe-104">句法</span><span class="sxs-lookup"><span data-stu-id="cdbbe-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cdbbe-105">說明</span><span class="sxs-lookup"><span data-stu-id="cdbbe-105">DESCRIPTION</span></span>
<span data-ttu-id="cdbbe-106">**AzLocation** Cmdlet 會取得所有位置，以及每個位置支援的資源提供者。</span><span class="sxs-lookup"><span data-stu-id="cdbbe-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="cdbbe-107">示例</span><span class="sxs-lookup"><span data-stu-id="cdbbe-107">EXAMPLES</span></span>

### <span data-ttu-id="cdbbe-108">範例1：取得所有位置及支援的資源提供者</span><span class="sxs-lookup"><span data-stu-id="cdbbe-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="cdbbe-109">這個命令會取得所有位置，以及每個位置支援的資源提供者。</span><span class="sxs-lookup"><span data-stu-id="cdbbe-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="cdbbe-110">參數</span><span class="sxs-lookup"><span data-stu-id="cdbbe-110">PARAMETERS</span></span>

### <span data-ttu-id="cdbbe-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cdbbe-111">-ApiVersion</span></span>
<span data-ttu-id="cdbbe-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="cdbbe-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="cdbbe-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="cdbbe-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbbe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdbbe-114">-DefaultProfile</span></span>
<span data-ttu-id="cdbbe-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cdbbe-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbbe-116">-預先</span><span class="sxs-lookup"><span data-stu-id="cdbbe-116">-Pre</span></span>
<span data-ttu-id="cdbbe-117">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="cdbbe-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cdbbe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdbbe-118">CommonParameters</span></span>
<span data-ttu-id="cdbbe-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cdbbe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdbbe-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cdbbe-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdbbe-121">輸入</span><span class="sxs-lookup"><span data-stu-id="cdbbe-121">INPUTS</span></span>

## <span data-ttu-id="cdbbe-122">輸出</span><span class="sxs-lookup"><span data-stu-id="cdbbe-122">OUTPUTS</span></span>

## <span data-ttu-id="cdbbe-123">筆記</span><span class="sxs-lookup"><span data-stu-id="cdbbe-123">NOTES</span></span>

## <span data-ttu-id="cdbbe-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdbbe-124">RELATED LINKS</span></span>
