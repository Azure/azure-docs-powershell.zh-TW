---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: a7c30ee436f35bee72e786c1d219e114236248da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452400"
---
# <span data-ttu-id="70fd1-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="70fd1-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="70fd1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="70fd1-103">取得資源提供者。</span><span class="sxs-lookup"><span data-stu-id="70fd1-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70fd1-104">句法</span><span class="sxs-lookup"><span data-stu-id="70fd1-104">SYNTAX</span></span>

### <span data-ttu-id="70fd1-105">ListAvailable (預設) </span><span class="sxs-lookup"><span data-stu-id="70fd1-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70fd1-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="70fd1-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70fd1-107">說明</span><span class="sxs-lookup"><span data-stu-id="70fd1-107">DESCRIPTION</span></span>
<span data-ttu-id="70fd1-108">**AzureRmResourceProvider** Cmdlet 會取得 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="70fd1-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="70fd1-109">示例</span><span class="sxs-lookup"><span data-stu-id="70fd1-109">EXAMPLES</span></span>

## <span data-ttu-id="70fd1-110">參數</span><span class="sxs-lookup"><span data-stu-id="70fd1-110">PARAMETERS</span></span>

### <span data-ttu-id="70fd1-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="70fd1-111">-ApiVersion</span></span>
<span data-ttu-id="70fd1-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="70fd1-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="70fd1-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="70fd1-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="70fd1-114">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="70fd1-114">-ListAvailable</span></span>
<span data-ttu-id="70fd1-115">表示此操作會取得所有可用的資源提供者。</span><span class="sxs-lookup"><span data-stu-id="70fd1-115">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="70fd1-116">-位置</span><span class="sxs-lookup"><span data-stu-id="70fd1-116">-Location</span></span>
<span data-ttu-id="70fd1-117">指定資源提供者的位置。</span><span class="sxs-lookup"><span data-stu-id="70fd1-117">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="70fd1-118">-預先</span><span class="sxs-lookup"><span data-stu-id="70fd1-118">-Pre</span></span>
<span data-ttu-id="70fd1-119">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="70fd1-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="70fd1-120">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="70fd1-120">-ProviderNamespace</span></span>
<span data-ttu-id="70fd1-121">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="70fd1-121">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: IndividualProvider
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70fd1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70fd1-122">-DefaultProfile</span></span>
<span data-ttu-id="70fd1-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70fd1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70fd1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70fd1-124">CommonParameters</span></span>
<span data-ttu-id="70fd1-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70fd1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70fd1-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="70fd1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70fd1-127">輸入</span><span class="sxs-lookup"><span data-stu-id="70fd1-127">INPUTS</span></span>

## <span data-ttu-id="70fd1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="70fd1-128">OUTPUTS</span></span>

### <span data-ttu-id="70fd1-129">PSResourceProvider 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="70fd1-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="70fd1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="70fd1-130">NOTES</span></span>

## <span data-ttu-id="70fd1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="70fd1-131">RELATED LINKS</span></span>

[<span data-ttu-id="70fd1-132">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="70fd1-132">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="70fd1-133">取消註冊-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="70fd1-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)

