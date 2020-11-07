---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0443b9bc3ed2666600f2d119eca5b7173b21e89d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625644"
---
# <span data-ttu-id="b352a-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b352a-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="b352a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b352a-102">SYNOPSIS</span></span>
<span data-ttu-id="b352a-103">建立 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="b352a-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b352a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b352a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b352a-105">說明</span><span class="sxs-lookup"><span data-stu-id="b352a-105">DESCRIPTION</span></span>
<span data-ttu-id="b352a-106">**新的-AzureRmApiManagementGroup** Cmdlet 會建立 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="b352a-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="b352a-107">示例</span><span class="sxs-lookup"><span data-stu-id="b352a-107">EXAMPLES</span></span>

### <span data-ttu-id="b352a-108">範例1：建立管理群組</span><span class="sxs-lookup"><span data-stu-id="b352a-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="b352a-109">這個命令會建立管理群組。</span><span class="sxs-lookup"><span data-stu-id="b352a-109">This command creates a management group.</span></span>

## <span data-ttu-id="b352a-110">參數</span><span class="sxs-lookup"><span data-stu-id="b352a-110">PARAMETERS</span></span>

### <span data-ttu-id="b352a-111">-內容</span><span class="sxs-lookup"><span data-stu-id="b352a-111">-Context</span></span>
<span data-ttu-id="b352a-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="b352a-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b352a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b352a-113">-DefaultProfile</span></span>
<span data-ttu-id="b352a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b352a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b352a-115">-描述</span><span class="sxs-lookup"><span data-stu-id="b352a-115">-Description</span></span>
<span data-ttu-id="b352a-116">指定管理群組的描述。</span><span class="sxs-lookup"><span data-stu-id="b352a-116">Specifies the description of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b352a-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="b352a-117">-ExternalId</span></span>
<span data-ttu-id="b352a-118">對於外部群組，此屬性包含來自外部身分識別提供者的群組識別碼，例如 Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c;否則，該值為 null。</span><span class="sxs-lookup"><span data-stu-id="b352a-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b352a-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="b352a-119">-GroupId</span></span>
<span data-ttu-id="b352a-120">指定新管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b352a-120">Specifies the identifier of the new management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b352a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b352a-121">-Name</span></span>
<span data-ttu-id="b352a-122">指定管理組名。</span><span class="sxs-lookup"><span data-stu-id="b352a-122">Specifies the management group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b352a-123">-類型</span><span class="sxs-lookup"><span data-stu-id="b352a-123">-Type</span></span>
<span data-ttu-id="b352a-124">群組類型。</span><span class="sxs-lookup"><span data-stu-id="b352a-124">Group Type.</span></span> <span data-ttu-id="b352a-125">[自訂群組] 是 [使用者定義] 群組。</span><span class="sxs-lookup"><span data-stu-id="b352a-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="b352a-126">系統群組包括管理員、開發人員和來賓。</span><span class="sxs-lookup"><span data-stu-id="b352a-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="b352a-127">您無法建立或更新系統群組。</span><span class="sxs-lookup"><span data-stu-id="b352a-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="b352a-128">[外部群組] 是來自于 Azure Active Directory 等外部身分識別提供者的群組。</span><span class="sxs-lookup"><span data-stu-id="b352a-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="b352a-129">這個參數是選擇性的，預設假設是自訂群組。</span><span class="sxs-lookup"><span data-stu-id="b352a-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: PsApiManagementGroupType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b352a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b352a-130">CommonParameters</span></span>
<span data-ttu-id="b352a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b352a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b352a-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b352a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b352a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b352a-133">INPUTS</span></span>

### <span data-ttu-id="b352a-134">所有</span><span class="sxs-lookup"><span data-stu-id="b352a-134">None</span></span>
<span data-ttu-id="b352a-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b352a-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b352a-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b352a-136">OUTPUTS</span></span>

### <span data-ttu-id="b352a-137">ServiceManagement. PsApiManagementGroup （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b352a-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="b352a-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b352a-138">NOTES</span></span>

## <span data-ttu-id="b352a-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b352a-139">RELATED LINKS</span></span>

[<span data-ttu-id="b352a-140">AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b352a-140">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="b352a-141">移除-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b352a-141">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="b352a-142">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b352a-142">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


