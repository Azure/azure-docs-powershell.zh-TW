---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: cc890bf13922069ac9f4d20d6a9e8d0c3aa04c94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795304"
---
# <span data-ttu-id="05be1-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="05be1-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="05be1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05be1-102">SYNOPSIS</span></span>
<span data-ttu-id="05be1-103">取得資源提供者。</span><span class="sxs-lookup"><span data-stu-id="05be1-103">Gets a resource provider.</span></span>

## <span data-ttu-id="05be1-104">句法</span><span class="sxs-lookup"><span data-stu-id="05be1-104">SYNTAX</span></span>

### <span data-ttu-id="05be1-105">ListAvailable (預設) </span><span class="sxs-lookup"><span data-stu-id="05be1-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05be1-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="05be1-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05be1-107">說明</span><span class="sxs-lookup"><span data-stu-id="05be1-107">DESCRIPTION</span></span>
<span data-ttu-id="05be1-108">**AzResourceProvider** Cmdlet 會取得 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="05be1-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="05be1-109">示例</span><span class="sxs-lookup"><span data-stu-id="05be1-109">EXAMPLES</span></span>

## <span data-ttu-id="05be1-110">參數</span><span class="sxs-lookup"><span data-stu-id="05be1-110">PARAMETERS</span></span>

### <span data-ttu-id="05be1-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="05be1-111">-ApiVersion</span></span>
<span data-ttu-id="05be1-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="05be1-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="05be1-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="05be1-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="05be1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05be1-114">-DefaultProfile</span></span>
<span data-ttu-id="05be1-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="05be1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05be1-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="05be1-116">-ListAvailable</span></span>
<span data-ttu-id="05be1-117">表示此操作會取得所有可用的資源提供者。</span><span class="sxs-lookup"><span data-stu-id="05be1-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="05be1-118">-位置</span><span class="sxs-lookup"><span data-stu-id="05be1-118">-Location</span></span>
<span data-ttu-id="05be1-119">指定資源提供者的位置。</span><span class="sxs-lookup"><span data-stu-id="05be1-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="05be1-120">-預先</span><span class="sxs-lookup"><span data-stu-id="05be1-120">-Pre</span></span>
<span data-ttu-id="05be1-121">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="05be1-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="05be1-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="05be1-122">-ProviderNamespace</span></span>
<span data-ttu-id="05be1-123">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="05be1-123">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="05be1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05be1-124">CommonParameters</span></span>
<span data-ttu-id="05be1-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05be1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05be1-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="05be1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05be1-127">輸入</span><span class="sxs-lookup"><span data-stu-id="05be1-127">INPUTS</span></span>

## <span data-ttu-id="05be1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="05be1-128">OUTPUTS</span></span>

## <span data-ttu-id="05be1-129">筆記</span><span class="sxs-lookup"><span data-stu-id="05be1-129">NOTES</span></span>

## <span data-ttu-id="05be1-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="05be1-130">RELATED LINKS</span></span>

[<span data-ttu-id="05be1-131">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="05be1-131">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="05be1-132">取消註冊-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="05be1-132">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


