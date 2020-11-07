---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ca4f9431a7b382166b99a33be5b9373871b610e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800030"
---
# <span data-ttu-id="6495f-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="6495f-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="6495f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6495f-102">SYNOPSIS</span></span>
<span data-ttu-id="6495f-103">取得資源提供者。</span><span class="sxs-lookup"><span data-stu-id="6495f-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6495f-104">句法</span><span class="sxs-lookup"><span data-stu-id="6495f-104">SYNTAX</span></span>

### <span data-ttu-id="6495f-105">ListAvailable (預設) </span><span class="sxs-lookup"><span data-stu-id="6495f-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6495f-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="6495f-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6495f-107">說明</span><span class="sxs-lookup"><span data-stu-id="6495f-107">DESCRIPTION</span></span>
<span data-ttu-id="6495f-108">**AzureRmResourceProvider** Cmdlet 會取得 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="6495f-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="6495f-109">示例</span><span class="sxs-lookup"><span data-stu-id="6495f-109">EXAMPLES</span></span>

## <span data-ttu-id="6495f-110">參數</span><span class="sxs-lookup"><span data-stu-id="6495f-110">PARAMETERS</span></span>

### <span data-ttu-id="6495f-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6495f-111">-ApiVersion</span></span>
<span data-ttu-id="6495f-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="6495f-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6495f-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="6495f-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="6495f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6495f-114">-DefaultProfile</span></span>
<span data-ttu-id="6495f-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6495f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6495f-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="6495f-116">-ListAvailable</span></span>
<span data-ttu-id="6495f-117">表示此操作會取得所有可用的資源提供者。</span><span class="sxs-lookup"><span data-stu-id="6495f-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6495f-118">-位置</span><span class="sxs-lookup"><span data-stu-id="6495f-118">-Location</span></span>
<span data-ttu-id="6495f-119">指定資源提供者的位置。</span><span class="sxs-lookup"><span data-stu-id="6495f-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="6495f-120">-預先</span><span class="sxs-lookup"><span data-stu-id="6495f-120">-Pre</span></span>
<span data-ttu-id="6495f-121">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="6495f-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6495f-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="6495f-122">-ProviderNamespace</span></span>
<span data-ttu-id="6495f-123">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="6495f-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6495f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6495f-124">CommonParameters</span></span>
<span data-ttu-id="6495f-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6495f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6495f-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6495f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6495f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="6495f-127">INPUTS</span></span>

## <span data-ttu-id="6495f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="6495f-128">OUTPUTS</span></span>

## <span data-ttu-id="6495f-129">筆記</span><span class="sxs-lookup"><span data-stu-id="6495f-129">NOTES</span></span>

## <span data-ttu-id="6495f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="6495f-130">RELATED LINKS</span></span>

[<span data-ttu-id="6495f-131">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="6495f-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="6495f-132">取消註冊-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="6495f-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


