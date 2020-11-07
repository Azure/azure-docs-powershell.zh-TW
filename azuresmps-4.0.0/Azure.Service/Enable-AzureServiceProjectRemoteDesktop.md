---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 163D2F00-E041-43A9-B077-9034F54B4F3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf258a8f13a344b09f9d5c7119cd78ad202d2ca0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967129"
---
# <span data-ttu-id="67047-101">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="67047-101">Enable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="67047-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67047-102">SYNOPSIS</span></span>
<span data-ttu-id="67047-103">啟用對雲端服務的遠端桌面存取。</span><span class="sxs-lookup"><span data-stu-id="67047-103">Enables remote desktop access to a cloud service.</span></span>

## <span data-ttu-id="67047-104">句法</span><span class="sxs-lookup"><span data-stu-id="67047-104">SYNTAX</span></span>

```
Enable-AzureServiceProjectRemoteDesktop -Username <String> -Password <SecureString> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="67047-105">說明</span><span class="sxs-lookup"><span data-stu-id="67047-105">DESCRIPTION</span></span>
<span data-ttu-id="67047-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67047-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="67047-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="67047-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="67047-108">**Enable-AzureServiceProjectRemoteDesktop** Cmdlet 可讓遠端桌面存取雲端服務。</span><span class="sxs-lookup"><span data-stu-id="67047-108">The **Enable-AzureServiceProjectRemoteDesktop** cmdlet enables Remote Desktop access to a cloud service.</span></span>
<span data-ttu-id="67047-109">您必須在啟用遠端桌面存取後使用 **Publish AzureServiceProject** Cmdlet 發佈服務，變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="67047-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after enabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="67047-110">示例</span><span class="sxs-lookup"><span data-stu-id="67047-110">EXAMPLES</span></span>

## <span data-ttu-id="67047-111">參數</span><span class="sxs-lookup"><span data-stu-id="67047-111">PARAMETERS</span></span>

### <span data-ttu-id="67047-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67047-112">-PassThru</span></span>
<span data-ttu-id="67047-113">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="67047-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="67047-114">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="67047-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="67047-115">-Password</span><span class="sxs-lookup"><span data-stu-id="67047-115">-Password</span></span>
<span data-ttu-id="67047-116">指定密碼。</span><span class="sxs-lookup"><span data-stu-id="67047-116">Specifies the password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: pwd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67047-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="67047-117">-Profile</span></span>
<span data-ttu-id="67047-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="67047-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67047-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="67047-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="67047-120">-Username</span><span class="sxs-lookup"><span data-stu-id="67047-120">-Username</span></span>
<span data-ttu-id="67047-121">指定透過遠端桌面通訊協定連線到 Azure 中的角色實例時要使用的使用者名稱 (RDP) 。</span><span class="sxs-lookup"><span data-stu-id="67047-121">Specifies the user name to use when connecting to the role instance in Azure via the Remote Desktop Protocol (RDP).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: user

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67047-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67047-122">CommonParameters</span></span>
<span data-ttu-id="67047-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67047-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67047-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67047-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67047-125">輸入</span><span class="sxs-lookup"><span data-stu-id="67047-125">INPUTS</span></span>

## <span data-ttu-id="67047-126">輸出</span><span class="sxs-lookup"><span data-stu-id="67047-126">OUTPUTS</span></span>

## <span data-ttu-id="67047-127">筆記</span><span class="sxs-lookup"><span data-stu-id="67047-127">NOTES</span></span>

## <span data-ttu-id="67047-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="67047-128">RELATED LINKS</span></span>

[<span data-ttu-id="67047-129">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="67047-129">Disable-AzureServiceProjectRemoteDesktop</span></span>](./Disable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="67047-130">發佈-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="67047-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


