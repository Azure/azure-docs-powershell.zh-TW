---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967538"
---
# <span data-ttu-id="a63a7-101">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a63a7-101">Remove-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="a63a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a63a7-102">SYNOPSIS</span></span>
<span data-ttu-id="a63a7-103">從流量管理器設定檔移除端點。</span><span class="sxs-lookup"><span data-stu-id="a63a7-103">Removes an endpoint from a Traffic Manager profile.</span></span>

## <span data-ttu-id="a63a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="a63a7-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a63a7-105">說明</span><span class="sxs-lookup"><span data-stu-id="a63a7-105">DESCRIPTION</span></span>
<span data-ttu-id="a63a7-106">**AzureTrafficManagerEndpoint** Cmdlet 會從 Microsoft Azure 流量管理器設定檔中移除端點。</span><span class="sxs-lookup"><span data-stu-id="a63a7-106">The **Remove-AzureTrafficManagerEndpoint** cmdlet removes an endpoint from a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="a63a7-107">移除端點之後，使用管線運算子將結果傳遞給 **AzureTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a63a7-107">After you remove an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a63a7-108">該 Cmdlet 會連線至 Azure 以儲存您的變更。</span><span class="sxs-lookup"><span data-stu-id="a63a7-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="a63a7-109">示例</span><span class="sxs-lookup"><span data-stu-id="a63a7-109">EXAMPLES</span></span>

### <span data-ttu-id="a63a7-110">範例1：從設定檔移除端點</span><span class="sxs-lookup"><span data-stu-id="a63a7-110">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="a63a7-111">第一個命令使用 **AzureTrafficManagerProfile** Cmdlet 來取得名為 ContosoProfile 的設定檔，然後將它儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="a63a7-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="a63a7-112">第二個命令會從 $TrafficManagerProfile 中儲存的流量管理器設定檔，移除具有 domain name Contoso02App.cloudapp.net 的端點。</span><span class="sxs-lookup"><span data-stu-id="a63a7-112">The second command removes an endpoint that has the domain name Contoso02App.cloudapp.net from the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="a63a7-113">命令會將設定檔物件傳遞給 **AzureTrafficManagerProfile** Cmdlet 以連線至 Azure，以儲存您的變更。</span><span class="sxs-lookup"><span data-stu-id="a63a7-113">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="a63a7-114">參數</span><span class="sxs-lookup"><span data-stu-id="a63a7-114">PARAMETERS</span></span>

### <span data-ttu-id="a63a7-115">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="a63a7-115">-DomainName</span></span>
<span data-ttu-id="a63a7-116">指定要移除之端點的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="a63a7-116">Specifies the domain name of the endpoint to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63a7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a63a7-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63a7-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a63a7-118">-Profile</span></span>
<span data-ttu-id="a63a7-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a63a7-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a63a7-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a63a7-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63a7-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a63a7-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="a63a7-122">指定要從中移除端點的流量管理員設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="a63a7-122">Specifies the Traffic Manager profile object from which to remove the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a63a7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63a7-123">CommonParameters</span></span>
<span data-ttu-id="a63a7-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a63a7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63a7-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a63a7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63a7-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a63a7-126">INPUTS</span></span>

## <span data-ttu-id="a63a7-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a63a7-127">OUTPUTS</span></span>

### <span data-ttu-id="a63a7-128">TrafficManager. IProfileWithDefinition （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="a63a7-128">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="a63a7-129">這個 Cmdlet 會產生流量管理器設定檔物件，其中包含已更新設定檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a63a7-129">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="a63a7-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a63a7-130">NOTES</span></span>

## <span data-ttu-id="a63a7-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a63a7-131">RELATED LINKS</span></span>

[<span data-ttu-id="a63a7-132">附加 AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a63a7-132">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="a63a7-133">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a63a7-133">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="a63a7-134">AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a63a7-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="a63a7-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a63a7-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


