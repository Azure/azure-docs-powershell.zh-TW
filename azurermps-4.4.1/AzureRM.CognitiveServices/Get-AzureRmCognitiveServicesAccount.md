---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: c4419707c9c536a21e5fdc8aa39326b02e21937c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449997"
---
# <span data-ttu-id="7c66b-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7c66b-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="7c66b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c66b-102">SYNOPSIS</span></span>
<span data-ttu-id="7c66b-103">取得帳戶。</span><span class="sxs-lookup"><span data-stu-id="7c66b-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c66b-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c66b-104">SYNTAX</span></span>

### <span data-ttu-id="7c66b-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c66b-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c66b-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c66b-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c66b-107">說明</span><span class="sxs-lookup"><span data-stu-id="7c66b-107">DESCRIPTION</span></span>
<span data-ttu-id="7c66b-108">**AzureRmCognitiveServicesAccount** Cmdlet 會取得 *ResoureGroupName* 參數所指定之資源群組中已預配的認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="7c66b-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="7c66b-109">如果您沒有指定 *ResoureGroupName* 參數，此 Cmdlet 會取得目前訂閱的所有認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="7c66b-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="7c66b-110">示例</span><span class="sxs-lookup"><span data-stu-id="7c66b-110">EXAMPLES</span></span>

## <span data-ttu-id="7c66b-111">參數</span><span class="sxs-lookup"><span data-stu-id="7c66b-111">PARAMETERS</span></span>

### <span data-ttu-id="7c66b-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c66b-112">-Name</span></span>
<span data-ttu-id="7c66b-113">指定要取得之認知服務帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c66b-113">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c66b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c66b-114">-ResourceGroupName</span></span>
<span data-ttu-id="7c66b-115">指定將 [認知服務] 帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c66b-115">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c66b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c66b-116">-DefaultProfile</span></span>
<span data-ttu-id="7c66b-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c66b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c66b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c66b-118">CommonParameters</span></span>
<span data-ttu-id="7c66b-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c66b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c66b-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c66b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c66b-121">輸入</span><span class="sxs-lookup"><span data-stu-id="7c66b-121">INPUTS</span></span>

## <span data-ttu-id="7c66b-122">輸出</span><span class="sxs-lookup"><span data-stu-id="7c66b-122">OUTPUTS</span></span>

### <span data-ttu-id="7c66b-123">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="7c66b-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="7c66b-124">筆記</span><span class="sxs-lookup"><span data-stu-id="7c66b-124">NOTES</span></span>

## <span data-ttu-id="7c66b-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c66b-125">RELATED LINKS</span></span>

[<span data-ttu-id="7c66b-126">新-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7c66b-126">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="7c66b-127">移除-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7c66b-127">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="7c66b-128">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7c66b-128">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


