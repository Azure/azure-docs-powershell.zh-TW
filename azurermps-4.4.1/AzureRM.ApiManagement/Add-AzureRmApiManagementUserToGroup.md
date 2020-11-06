---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: d405dc21719abc1aec5767f4d1b89a938b79eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447203"
---
# <span data-ttu-id="58be5-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="58be5-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="58be5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58be5-102">SYNOPSIS</span></span>
<span data-ttu-id="58be5-103">將使用者新增至群組。</span><span class="sxs-lookup"><span data-stu-id="58be5-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58be5-104">句法</span><span class="sxs-lookup"><span data-stu-id="58be5-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58be5-105">說明</span><span class="sxs-lookup"><span data-stu-id="58be5-105">DESCRIPTION</span></span>
<span data-ttu-id="58be5-106">**AzureRmApiManagementUserToGroup** Cmdlet 會將使用者新增至群組。</span><span class="sxs-lookup"><span data-stu-id="58be5-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="58be5-107">示例</span><span class="sxs-lookup"><span data-stu-id="58be5-107">EXAMPLES</span></span>

### <span data-ttu-id="58be5-108">範例1：將使用者新增至群組</span><span class="sxs-lookup"><span data-stu-id="58be5-108">Example 1: Add a user to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="58be5-109">這個命令會將現有的使用者新增至現有的群組。</span><span class="sxs-lookup"><span data-stu-id="58be5-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="58be5-110">參數</span><span class="sxs-lookup"><span data-stu-id="58be5-110">PARAMETERS</span></span>

### <span data-ttu-id="58be5-111">-內容</span><span class="sxs-lookup"><span data-stu-id="58be5-111">-Context</span></span>
<span data-ttu-id="58be5-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="58be5-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="58be5-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="58be5-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58be5-114">-GroupId</span><span class="sxs-lookup"><span data-stu-id="58be5-114">-GroupId</span></span>
<span data-ttu-id="58be5-115">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="58be5-115">Specifies the group ID.</span></span>
<span data-ttu-id="58be5-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="58be5-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58be5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58be5-117">-PassThru</span></span>
<span data-ttu-id="58be5-118">passthru</span><span class="sxs-lookup"><span data-stu-id="58be5-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58be5-119">-UserId</span><span class="sxs-lookup"><span data-stu-id="58be5-119">-UserId</span></span>
<span data-ttu-id="58be5-120">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="58be5-120">Specifies the user ID.</span></span>
<span data-ttu-id="58be5-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="58be5-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58be5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58be5-122">-DefaultProfile</span></span>
<span data-ttu-id="58be5-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58be5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58be5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58be5-124">CommonParameters</span></span>
<span data-ttu-id="58be5-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58be5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58be5-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58be5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58be5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="58be5-127">INPUTS</span></span>

## <span data-ttu-id="58be5-128">輸出</span><span class="sxs-lookup"><span data-stu-id="58be5-128">OUTPUTS</span></span>

### <span data-ttu-id="58be5-129">布林值</span><span class="sxs-lookup"><span data-stu-id="58be5-129">Boolean</span></span>

## <span data-ttu-id="58be5-130">筆記</span><span class="sxs-lookup"><span data-stu-id="58be5-130">NOTES</span></span>

## <span data-ttu-id="58be5-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="58be5-131">RELATED LINKS</span></span>

[<span data-ttu-id="58be5-132">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="58be5-132">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="58be5-133">移除-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="58be5-133">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


